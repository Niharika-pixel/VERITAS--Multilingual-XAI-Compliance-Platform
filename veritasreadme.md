# Veritas — Multilingual XAI Compliance Console

A single-file, front-end demo console for inspecting AI-driven decisions with multilingual explanations, factor attributions, risk scores, compliance checks, and printable audit reports.

## Features

- **Decision list** — browse sample AI decisions across lending, insurance, and recruitment use cases
- **Contributing factors** — visual attribution bars showing what supported or opposed each decision
- **Plain-language explanations** — human-readable rationale for every outcome
- **Compliance checklist** — right-to-explanation, protected-attribute usage, and record-retention status
- **Multilingual UI** — switch instantly between English, Hindi (हिंदी), and Marathi (मराठी)
- **Printable audit reports** — the "Generate audit report" button opens a print-ready view (Ctrl/Cmd+P → Save as PDF)
- **Analyze New Decision** — enter your own decision (type, applicant/ID, model, outcome, confidence, income, credit score, debt-to-income ratio, other factors, optional context) and get a generated analysis, added straight to the decision list

### About "Analyze New Decision"

This feature is a **prototype, not a live model**. Every decision created through the form is:

- Labeled with a **"Prototype"** tag in the sidebar and a banner on its detail page
- Explained using **only the values you enter** — no fabricated numbers, reasoning, or attribution weights
- Given a **risk level estimated from your stated confidence score** (`risk score = 100 − confidence`), clearly marked as a heuristic rather than a model output
- Fully translated for the English/Hindi/Marathi selector, **except** free-text fields (applicant name, decision type, other factors, context), which are shown exactly as typed since there's no translation backend — the app notes this rather than guessing a translation
- Checked against the same compliance checklist as the built-in decisions
- Supported by the same "Generate audit report" print flow

## Tech

Plain HTML, CSS, and vanilla JavaScript — no build step, no dependencies, no external requests. Everything needed to run lives in `veritas.html`.

## Running locally

Just open `veritas.html` in any modern browser. No server or install required.

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to your default branch (e.g. `main`) and folder `/ (root)`.
4. GitHub Pages serves whatever is named `index.html` at the repo root as the homepage. Since this file is named `veritas.html`, either:
   - rename it to `index.html` before pushing, **or**
   - keep the name and link to it directly at `https://<your-username>.github.io/<repo-name>/veritas.html`

## Data

All built-in decisions, factors, and translations in this demo are **sample/mock data** for illustration purposes only — not connected to a real model or backend. Decisions created via "Analyze New Decision" use only the data you type into the form.

## License

MIT (or update to your preference).
