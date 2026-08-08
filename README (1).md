# Veritas — Multilingual XAI Compliance Console

A single-file, front-end demo console for inspecting AI-driven decisions with multilingual explanations, factor attributions, risk scores, compliance checks, and printable audit reports.

## Features

- **Decision list** — browse sample AI decisions across lending, insurance, and recruitment use cases
- **Contributing factors** — visual attribution bars showing what supported or opposed each decision
- **Plain-language explanations** — human-readable rationale for every outcome
- **Compliance checklist** — right-to-explanation, protected-attribute usage, and record-retention status
- **Multilingual UI** — switch instantly between English, Hindi (हिंदी), and Marathi (मराठी)
- **Printable audit reports** — the "Generate audit report" button opens a print-ready view (Ctrl/Cmd+P → Save as PDF)

## Tech

Plain HTML, CSS, and vanilla JavaScript — no build step, no dependencies, no external requests. Everything needed to run lives in `index.html`.

## Running locally

Just open `index.html` in any modern browser. No server or install required.

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to your default branch (e.g. `main`) and folder `/ (root)`.
4. Save — GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/`.

## Data

All decisions, factors, and translations in this demo are **sample/mock data** for illustration purposes only — not connected to a real model or backend.

## License

MIT (or update to your preference).
