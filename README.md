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

