# ATS Score Checker


> A fully client-side ATS (Applicant Tracking System) score checker that analyzes your resume against a job description and gives AI-powered improvement advice — no server, no data collection.

🔗 **Live Demo:** [ats-score-checker-cxl6.vercel.app](https://ats-score-checker-cxl6.vercel.app/)

---

## What It Does

Paste or upload your resume and a job description, and ATS::SCAN will:

- **Score your resume** from 0–100 based on ATS compatibility
- **Break down your score** across key categories (keyword match, formatting, structure, etc.)
- **Identify matched and missing keywords** — so you know exactly what to add
- **Surface actionable findings** — critical issues, warnings, and what you're doing right
- **Generate an AI-powered improvement plan** using your own API key (optional — Step 3 only)

---

## Features

- **3-step pipeline** — Input → Scan → Advisory
- **File upload support** — paste text or drop `.PDF`, `.DOCX`, or `.TXT` files
- **Keyword analysis** — matched keywords shown in green, missing ones in red
- **Category score meters** — visual breakdown of where your resume stands
- **Multi-provider AI advisory** — plug in your own key for Anthropic, OpenAI, Gemini, or any OpenAI-compatible endpoint
- **100% client-side** — nothing leaves your browser except Step 3 AI calls, which go directly to your chosen provider
- **Animated radar background** — because why not look cool while fixing your resume
- **No dependencies** — single `index.html` file, zero npm, zero build step

---

## Privacy

> Your resume and job description never touch any third-party server (other than the AI provider you configure in Step 3). All scoring logic runs entirely in your browser via JavaScript.

---

## How to Use

### Online (recommended)
Just visit **[ats-score-checker-cxl6.vercel.app](https://ats-score-checker-cxl6.vercel.app/)** — no install needed.

### Run Locally
```bash
git clone https://github.com/YOUR_USERNAME/ats-score-checker.git
cd ats-score-checker
# Open index.html in your browser — that's it.
open index.html
```

No Node, no Python, no package manager required.

---

## AI Advisory (Optional)

Step 3 generates a personalized improvement plan using an LLM. To enable it:

1. Click the **⚙ Settings** gear icon (top right)
2. Choose your AI provider and enter your API key
3. Keys are stored in your **browser's localStorage only** — never sent anywhere except directly to the provider

| Provider | Model Used | Where to Get Key |
|---|---|---|
| Anthropic | claude-sonnet-4-6 | [console.anthropic.com](https://console.anthropic.com) |
| OpenAI | gpt-4o-mini | [platform.openai.com](https://platform.openai.com) |
| Gemini | gemini-2.0-flash | [aistudio.google.com](https://aistudio.google.com) |
| Custom | Any model | Your own OpenAI-compatible endpoint |

---

## Tech Stack

| Layer | Tech |
|---|---|
| UI | Vanilla HTML/CSS/JS — single file |
| Fonts | JetBrains Mono + Inter (Google Fonts) |
| Background | Canvas 2D — animated radar/network effect |
| AI calls | Fetch API → provider of your choice |
| Hosting | Vercel (static) |

---

## File Structure

```
ats-score-checker/
└── index.html     # The entire app — self-contained
```

---

## Deployment (Vercel)

1. Fork or clone this repo
2. Go to [vercel.com](https://vercel.com) → **New Project** → Import your repo
3. Framework preset: **None** (it's just a static HTML file)
4. Deploy — done 

---

## Contributing

Issues and PRs are welcome. If you find a bug or have a feature idea, open an issue and describe it clearly.

---

## License

MIT License — free to use, modify, and deploy.

---

*Created by **Boltx***
