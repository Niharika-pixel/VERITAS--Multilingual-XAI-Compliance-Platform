# 🙏 SchemeSaathi

**Find every government scheme you actually qualify for — in English or Hindi, in under 2 minutes.**

Built for the **Girls In STEM Global Hackathon 2026**.

🔗 **Live demo:** _[add your deployed link here]_
📽️ **Demo video:** _[add your Devpost demo video link here]_

---

## The problem

India runs 100+ central and state welfare schemes — scholarships, health insurance, farming subsidies, business loans, savings schemes for girls — but most eligible people never find out these exist. Information is scattered across dozens of government websites, written in dense bureaucratic language that assumes English fluency and digital literacy neither of which are guaranteed for the people who need this help most.

## The solution

SchemeSaathi replaces the search-and-decode process with a short, friendly, one-question-at-a-time flow. No forms, no jargon, no typing required for most questions — just big tappable buttons. Answer six simple questions about yourself, and a matching algorithm shows exactly which schemes you qualify for, with a direct link to the real official government website to apply.

Built with a **Girls in STEM** audience in mind, it includes a dedicated spotlight section for schemes aimed at women and girls, and every part of the interface — questions, results, and even the chatbot — works in both **English and Hindi**.

## Features

- 🧭 **Step-by-step eligibility finder** — one plain-language question at a time, answered by tapping icons, not typing
- 🎯 **Matching algorithm** — scores each of the 11 schemes in the database against your answers (age, gender, occupation, category, income, and whether you have a young daughter) and ranks them as a "strong match" or "worth checking"
- 🌐 **English / Hindi toggle** — every question, scheme, and chatbot reply switches language instantly, mid-flow, without losing your answers
- ✨ **Women & Girls spotlight** — a dedicated section highlighting schemes most likely to go unclaimed simply from lack of awareness
- 📋 **Browse all schemes** — a searchable list for anyone who'd rather explore manually
- 💬 **Built-in assistant chatbot** — answers common questions about how matching works, what documents are needed, and data privacy, in either language
- 🔗 **Direct apply links** — every scheme links straight to its real, official `.gov.in` application portal

## How it works (the "AI")

Each scheme has a small set of eligibility rules (e.g. *occupation = farmer*, *income ≤ ₹1.5 lakh*). When you answer the questions, SchemeSaathi checks how many of a scheme's rules your answers satisfy:

```
match score = (rules you satisfy) ÷ (total rules for that scheme)
```

- **Score = 100%** → shown as a ✅ Strong match
- **Score = 50–99%** → shown as a 👍 Worth checking
- Below 50% → not shown, to avoid misleading anyone

This is a transparent, explainable content-based matching approach — not a black box — so it's easy to audit and easy to extend with more schemes and rules over time.

## Tech stack

- **HTML5 / CSS3 / Vanilla JavaScript** — no frameworks, no build step
- **Google Fonts** — Fraunces, Work Sans, Noto Sans Devanagari
- No backend, no database, no external APIs — everything runs client-side in the browser, and nothing typed by a user is ever sent or stored anywhere

## Project structure

Everything lives in a single file:

```
index.html   → all HTML, CSS, and JavaScript
```

Key parts inside `index.html`:

| Section | What it does |
|---|---|
| `SCHEMES` | The database of 11 government schemes, each with bilingual name/benefit/eligibility text, an official apply link, and eligibility rule functions |
| `T` | The English/Hindi translation dictionary for every UI string |
| `showStep()` / `renderResults()` | Drives the step-by-step wizard and the matching engine |
| `renderSpotlight()` / `renderBrowse()` | Renders the Women & Girls spotlight and the full searchable scheme list |
| `botReply()` / `addMsg()` | Powers the keyword-matched assistant chatbot |
| `applyLanguage()` | Swaps every piece of text on the page when the EN/हिं toggle is used |

## Running it locally

No installation needed — it's a static file.

```bash
# just open it directly
open index.html

# or serve it locally
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying it

Drag-and-drop the file at [app.netlify.com/drop](https://app.netlify.com/drop), or push it to a GitHub repo and enable GitHub Pages (Settings → Pages → deploy from `main`).

## Disclaimer

Scheme details (eligibility, benefits, and links) are drawn from publicly available government information and simplified for clarity. Rules, amounts, and deadlines change — SchemeSaathi is a discovery tool to point people in the right direction, not an official eligibility confirmation. Always verify on the official portal before applying.

## Team

_[add your team members' names here]_

## Acknowledgements

Built for the **Girls In STEM Global Hackathon 2026**, under the **Community Resources** theme, to help close the awareness gap around government entitlements in India.
