# AI PDF Summarizer

A single-file web app that summarizes PDF documents using AI. Drop a PDF, the app extracts its text in the browser (pdf.js) and sends it to an LLM via OpenRouter for a concise summary — all from one `index.html`.

## Features

- Drag-and-drop or file-picker PDF upload
- In-browser text extraction with pdf.js (nothing uploaded to a server)
- AI summarization via the OpenRouter chat API
- Clean single-file UI — no build step

## Tech Stack

- Single HTML file (HTML + Tailwind CSS + vanilla JS)
- pdf.js (CDN) for text extraction
- OpenRouter API for summarization

## Quick Start

Just open `index.html` in a browser — or serve it:

```bash
npx serve .
```

## ⚠️ Security Note

The app currently has an **API key embedded directly in `index.html`**. Before sharing or deploying widely:

1. Replace it with your own OpenRouter API key, or
2. Better: remove the embedded key and add a key-input field so each user supplies their own, or
3. Proxy the API call through your own backend.

Then **rotate/revoke the exposed key** in your OpenRouter dashboard — it is visible in git history.

## Project Structure

```
├── index.html   # The entire app — upload, extraction, summarization
└── README.md
```

## Deploy

Fully static — host `index.html` on any static host (GitHub Pages, Cloudflare Pages, Netlify).

---

Built by Girish Lade — https://ladestack.in
