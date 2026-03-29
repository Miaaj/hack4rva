# 🏛️ Richmond Contract Navigator

**Hack for RVA 2026 · Pillar 4: Thriving Economy**

[![Hackathon](https://img.shields.io/badge/Hack%20for%20RVA-2026-C8102E)](https://hack-for-rva.devpost.com)
[![Pillar](https://img.shields.io/badge/Pillar-Thriving%20Economy-1B2A4A)](https://github.com/hack4rva/pillar-thriving-economy)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue)](LICENSE)

---

## What It Does

Richmond Contract Navigator is an AI-powered, single-file web app that helps **minority-owned and first-time businesses** in Richmond, VA find and understand City contracting opportunities — in plain English.

The City of Richmond publishes procurement opportunities publicly, but the listings are written for vendors who already understand government contracting. Most small and minority-owned businesses struggle to determine which opportunities are relevant, interpret procurement terminology, or know what to do first.

This tool acts as a **matching and translation layer** between the business owner and the City's open procurement data. It does not replace the official City portal — it makes it more accessible.

### Core Features

- **AI-powered matching** — Describe your business in plain English and get matched to relevant City contracts using the Claude API
- **Jargon translation** — Every result explains what the contract actually means in simple terms
- **Why it matched** — Shows exactly which keywords from your description triggered each match
- **Vendor readiness checklist** — Interactive, contract-specific checklist of steps to take before bidding
- **First step guidance** — One clear, concrete action per result
- **Vendor Readiness Roadmap** — Universal steps to becoming a City contractor
- **Procurement glossary** — Plain-English definitions of IFB, RFP, bonding, pre-bid meetings, and more
- **City resource links** — Direct links to the Office of Minority Business Development, Economic Development, Procurement Services, and Community Wealth Building
- **Get Notified** — Opens a pre-filled email to request contract alerts
- **Print / Save PDF** — Save or print full results for offline use
- **Live streaming responses** — AI results stream in real time so you see progress immediately

### What It Does NOT Do

- Make eligibility determinations
- Suggest or award contracts
- Replace the official City vendor portal
- Require any backend server or database

---

## Data Sources

| Source | Description |
|---|---|
| [City of Richmond Contracts Registry](https://data.richmondgov.com/Well-Managed-Government/City-Contracts/xqn7-jvv2) | Socrata dataset `xqn7-jvv2` — open procurement data |
| [City Vendor Portal](https://mvendor.cgieva.com/Vendor/public/AllOpportunities.jsp?&agencyname=City%20of%20Richmond%20Government) | Official live solicitations — authoritative source |

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML, CSS, JavaScript — no frameworks |
| AI | Anthropic Claude API (Haiku model) with streaming |
| Data | City of Richmond Open Data Portal (Socrata) |
| Hosting | Any static file host, or open directly in browser |

---

## Getting Started

### Requirements

- A modern web browser (Chrome, Edge, Safari, Firefox)
- An **Anthropic API key** — [get one at console.anthropic.com](https://console.anthropic.com)

> ⚠️ **You must supply your own Anthropic API key.** The app does not include a key. API usage is billed per token to your Anthropic account. For typical demo usage, costs are well under $1.

### Running the App

1. Download `richmond-contract-navigator.html`
2. Open it by double-clicking — it runs entirely in your browser
3. Click **⚙ API Key** in the top-right corner
4. Paste your Anthropic API key and click **Save**
5. Describe your business and click **🔍 Find Matching Contracts**

No installation, no server, no dependencies.

### API Key Security

- Your API key is saved to your browser's `localStorage` — it never leaves your device
- Never paste your API key into a chat, email, or public forum
- If you accidentally expose a key, revoke it immediately at [console.anthropic.com](https://console.anthropic.com) and generate a new one

---

## How It Works

```
User describes business
        ↓
Optional profile fields (MBE status, employees, first bid?)
        ↓
App loads curated Richmond contract data
        ↓
Prompt sent to Claude API (Haiku model, streaming)
        ↓
AI matches business to top 3 contracts
        ↓
Results streamed live to the browser
        ↓
Each result rendered with:
  — Plain-English explanation
  — Why it matched
  — Vendor readiness checklist
  — First step
        ↓
Supporting resources shown:
  — Vendor Readiness Roadmap
  — Portal links
  — City help resources
  — Procurement glossary (on demand)
```

---

## Project Structure

```
richmond-contract-navigator.html   ← entire app in one file
README.md                          ← this file
```

---

## Judging Alignment — Pillar 4: Thriving Economy

| Rubric Category | How This Project Addresses It |
|---|---|
| **Impact** | Directly addresses MBE contracting access — the #1 scored problem in the pillar |
| **User Value** | Built for a specific user: first-time MBE contractor with no government contracting experience |
| **Feasibility** | No City systems required, public data only, zero ongoing maintenance burden |
| **Innovation** | AI-powered jargon translation + matching is a novel approach to procurement access |
| **Execution** | Fully working prototype with live API, streaming, interactive checklists, and real data links |
| **Equity & Inclusion** | Designed specifically for minority-owned businesses, plain language throughout, MBE/WBE resources surfaced |

---

## Disclaimer

This tool is **not an official City of Richmond service**. It does not determine eligibility, make contract award recommendations, or replace the City's official vendor portal. Always verify details through official City channels.

---

## Built By

**Mia Wang - Lotus Love LLC** · Williamsburg, VA
Richmond Civic Hackathon · March 27–29, 2026 · VCU Snead Hall

---

## License

Apache 2.0 — see [LICENSE](LICENSE) for details.
