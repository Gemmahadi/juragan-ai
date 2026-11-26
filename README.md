# Juragan AI — Autonomous Agent for Indonesian Warung (UMKM)

> Submission for the **Zyrelyx Global AI Hackathon** (Devpost, Dec 1–7 2026).
> One autonomous AI employee for a small Indonesian warung: it serves customers,
> keeps the debt ledger, watches stock, and reports to the owner — on its own.

## What it does (MVP)

- **Customer Agent** — chats with customers (WhatsApp-style), answers stock/price
  questions, takes orders, totals the bill.
- **Ledger Agent** — records debts & purchases into the cash book (SQLite),
  including from voice notes ("Budi hutang kopi 2, 10 ribu" → ledger row).
  Sends due-date reminders.
- **Stock Agent** — watches stock levels, alerts when items run low, suggests
  restock orders with estimated capital.
- **Owner Dashboard** — live activity feed of everything the agents did,
  approvals for sensitive actions, daily summary (revenue, collectible debt).

Every agent action is logged (audit trail) — the owner can always see *why*
the agent did what it did.

## Tech

- Frontend: React (Vite) — Vercel
- Backend: Node.js + TypeScript — Render
- LLM: Google Gemini 2.5 Flash (free tier) — agent reasoning & tool use
- DB: SQLite + seed data of a realistic Indonesian warung (prices in IDR)
- Voice input: Web Speech API

## Status

Sprint: **Dec 1, 2026 15:00 WIB – Dec 8, 2026 14:59 WIB**.
Core code, prompts and agent logic are developed during the sprint, per the
hackathon rules. This repo was created pre-sprint with only this README,
license and folder skeleton (allowed starter scaffolding).

## Run it (after the sprint)

```bash
cp .env.example .env   # set GEMINI_API_KEY
npm install
npm run dev
```

## License

MIT
