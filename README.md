# FUUM — Reward Layer for Quality on Base

FUUM (Fake It Until U Make It) is the **reward layer for quality** on the @baseapp.  
The **FAKE engine** (Forensic Anti-bot & Knowledge Evaluation) identifies high-quality content and miniapps, then FUUM rewards them.

---

## ⚙️ Tech Stack (ASCII diagram)

            ┌───────────────────────────┐
            │        User Layer         │
            │    (Web / Mobile App)     │
            └──────────────┬────────────┘
                           │
            ┌──────────────▼─────────────┐
            │     Frontend (Client)      │
            │ ReactJS • TypeScript •     │
            │ TailwindCSS • OnchainKit • │
            │ Neynar (social/identity)   │
            └──────────────┬─────────────┘
                           │
            ┌──────────────▼─────────────┐
            │     App / API Services     │
            │ Node.js (FUUM APIs) •      │
            │ FastAPI (FAKE scoring API) │
            │ Realtime Pub/Sub (e.g. WS) │
            └──────────────┬─────────────┘
                           │
            ┌──────────────▼─────────────┐
            │        FAKE Engine         │
            │ ML for authenticity,       │
            │ utility, quality, novelty  │
            │ Vector DB (embeddings)     │
            │ Feature Store + ETL        │
            └──────────────┬─────────────┘
                           │
            ┌──────────────▼─────────────┐
            │   Data & Storage Layer     │
            │ PostgreSQL • Redis (cache) │
            │ Object Store (logs/Parquet)│
            │ IPFS/Arweave (assets)      │
            └──────────────┬─────────────┘
                           │
            ┌──────────────▼─────────────┐
            │   Smart Contracts (Base)   │
            │ Solidity: VouchRegistry    │
            │ FAKE Oracle • FUUM Minter  │
            │ ClusterGuard • NFTs/Passes │
            └──────────────┬─────────────┘
                           │
            ┌──────────────▼─────────────┐
            │      Base L2 Blockchain    │
            └────────────────────────────┘

---

## 🗺️ Tech Stack (Mermaid diagram)

> GitHub renders Mermaid automatically in Markdown.

```mermaid
flowchart TB
  A[User Layer<br/>(Web / Mobile App)] --> B[Frontend (Client)<br/>React • TS • TailwindCSS • OnchainKit • Neynar]
  B --> C[App / API Services<br/>Node (FUUM APIs) • FastAPI (FAKE Scoring) • Realtime Pub/Sub]
  C --> D[FAKE Engine<br/>ML authenticity/quality/novelty • Vector DB (embeddings) • Feature Store/ETL]
  D --> E[Data & Storage<br/>PostgreSQL • Redis • Object Store • IPFS/Arweave]
  C --> F[Smart Contracts (Base)<br/>Solidity: VouchRegistry • FAKE Oracle • FUUM Minter • ClusterGuard • NFTs]
  F --> G[Base L2 Blockchain]

## 4) Commit the changes
1. Scroll to the bottom of the editor.
2. **Commit message:** `Add FUUM stack diagrams (ASCII + Mermaid)`
3. Click **Commit changes**.

## 5) Verify it looks right
- You’ll land back on the README view.
- The **ASCII** block shows as plain text with boxes.
- The **Mermaid** block should render as a diagram (give the page a quick refresh if it doesn’t show instantly).

## 6) Share it
- Copy the repo URL from your browser (e.g., `https://github.com/yourname/fuum`) and share it anywhere (Base app, X, investor docs).

---

### Pro tips (optional)
- Want a docs site? Enable **GitHub Pages** (Settings → Pages) and add more `.md` files in a `/docs` folder.
- Keep diagrams small and focused—create separate sections for **FAKE Engine** internals or **on-chain contracts** later.

If you want, I can also give you a **Mermaid diagram just for the FAKE Engine internals** so you can add it as a second diagram in the README.
# FUUM
A reward layer for quality on base 
