# Xero Coaching Hub

A team coaching dashboard for Xero partner sales managers. Track quota attainment, Gong call quality, capability ratings, GROW coaching plans, pipeline, and coaching notes for every AE on your team — and generate AI meeting prep briefs.

**Companion site:** [Xero Change Management workspace](https://xero-change-management.vercel.app/) — playbooks, training, and templates linked throughout the dashboard.

## How it works

This is a single static HTML file (`index.html`). There is no backend and no database.

- **All data lives in your browser** (localStorage). Nothing you enter is sent to a server, and nobody else can see your data — even on the shared URL.
- The hosted site ships with **fictional demo data** so anyone can explore it safely.
- Each manager loads their own real data via **Import CSV** (Salesforce / Gong exports), **Import JSON**, or **Sync from Glean**.

## Features

- **Team dashboard** — quota, Gong scores, coaching activity at a glance
- **AE profiles** — overview, Gong calls, Salesforce pipeline & activity, capability ratings, GROW coaching plan, coaching notes
- **AI call analysis** — paste a transcript, get scored skills, key moments, and a coaching recommendation (requires an Anthropic API key)
- **Meeting prep generator** — builds a pre-call brief from your stored calls and Glean (requires API keys)
- **Recommended training** — each coaching plan links to matching pages in the Change Management workspace
- **Import/Export** — CSV wizard for Salesforce and Gong exports, JSON backup/restore

## API keys (optional)

AI features need an [Anthropic API key](https://console.anthropic.com/); Glean sync needs a Glean API token. Set both via **API Keys** in the sidebar. Keys are stored only in your browser's localStorage and are never included in exports.

> Note: when the page is hosted online, some browsers block direct Glean API calls (CORS). If Glean sync fails, use Import CSV instead.

## Run locally

Open `index.html` in a browser. That's it.

## Deploy

Any static host works. For Vercel: import the repo, framework preset **Other**, no build command, output directory `.`.

---

V1 — June 2026. Owned by Harvey Patterson, Xero commercial.
