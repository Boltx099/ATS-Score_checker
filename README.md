# ATS Score Checker

An AI-powered Applicant Tracking System (ATS) resume analyzer built as a single-file interactive web widget. Paste or upload your resume and a job description to instantly get a compatibility score, keyword gap analysis, and Claude AI-generated improvement advice.

---

## Features

- **ATS compatibility scoring** — scores your resume out of 100 across 5 weighted categories
- **Keyword analysis** — extracts top keywords from the job description and shows what your resume is missing
- **AI-powered improvement plan** — uses the Claude API to generate personalized, role-specific advice with before/after bullet rewrites
- **File upload support** — drag and drop or click to upload `.pdf`, `.docx`, or `.txt` files
- **3-step flow** — clean Input → Score → AI Advice navigation
- **Dark mode ready** — fully adapts to light and dark themes

---

## Scoring Breakdown

| Category | Weight | What it checks |
|---|---|---|
| Keyword relevance | 40% | How many JD keywords appear in your resume |
| Action verbs | 20% | Use of strong verbs like "Led", "Built", "Optimized" |
| Quantified results | 15% | Metrics like percentages, numbers, team sizes |
| Resume structure | 15% | Section headers, bullet points |
| Length & density | 10% | Word count (400–900 is ideal) |

---

## Tech Stack

| Layer | Technology |
|---|---|
| UI | Vanilla HTML, CSS, JavaScript |
| PDF parsing | [PDF.js](https://mozilla.github.io/pdf.js/) v3.11 |
| DOCX parsing | [Mammoth.js](https://github.com/mwilliamson/mammoth.js/) v1.6 |
| AI feedback | [Anthropic Claude API](https://docs.anthropic.com/) (claude-sonnet-4-6) |
| Icons | [Tabler Icons](https://tabler.io/icons) (outline webfont) |

---

## Getting Started

### Option 1 — Run locally

Clone the repo and open `index.html` in your browser. No build step or server required.

```bash
git clone https://github.com/your-username/ats-score-checker.git
cd ats-score-checker
open index.html
```

### Option 2 — Deploy to GitHub Pages

1. Go to your repo **Settings → Pages**
2. Set source to `main` branch, `/ (root)`
3. Your checker will be live at `https://your-username.github.io/ats-score-checker`

---

## Usage

1. **Paste or upload** your job description (left panel)
2. **Paste or upload** your resume — supports `.pdf`, `.docx`, `.txt`
3. Click **Analyze resume** to get your ATS score and keyword breakdown
4. Click **Get AI-powered advice** for a Claude-generated improvement plan

---

## Project Structure

```
ats-score-checker/
├── index.html       # Main app (single file — all HTML, CSS, JS included)
└── README.md
```

---

## Notes

- The AI advice feature calls the Anthropic API directly from the browser. This works out of the box inside Claude.ai artifacts. If you host it externally, you will need to proxy the API call through a backend to keep your API key secure.
- File parsing runs entirely in the browser — no files are uploaded to any server.
- The scoring algorithm is heuristic-based and designed to approximate real ATS behavior. Results are indicative, not definitive.

---

## License

MIT — free to use, modify, and distribute.

---

## Author

Built by [Bolt](https://github.com/your-username)
