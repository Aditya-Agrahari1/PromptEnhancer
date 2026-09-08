<p align="center">
  <img src="Web/Images/keen.png" alt="Keen" width="120">
</p>

<h1 align="center">Keen</h1>
<p align="center"><em>every prompt, sharper.</em></p>

<p align="center">
  <img src="https://img.shields.io/badge/Chrome_Extension-Manifest_V3-4285F4?style=flat-square&logo=googlechrome&logoColor=white" alt="Chrome Extension" />
  <img src="https://img.shields.io/badge/Platforms-Claude_%7C_ChatGPT_%7C_Gemini_%7C_Perplexity-8B5CF6?style=flat-square" alt="Platforms" />
  <img src="https://img.shields.io/badge/Status-Live_on_Chrome_Web_Store-22C55E?style=flat-square" alt="Status" />
</p>

---

**Keen** is a Chrome extension that turns vague prompts into expert-level instructions — the kind a domain specialist would have written if they'd taken the time — before you hit send.

> **This is not a "rewrite my sentence" tool.**
> Most prompt enhancers run your text through a generic "make it better" template. Keen uses a multi-stage intelligence pipeline that understands *what* you're asking, *which domain* it belongs to, and *where* you're sending it — then adapts its entire strategy accordingly.

---

## Why This Is Different

| Most prompt enhancers | Keen |
|---|---|
| One-size-fits-all "improve this" template | Multi-stage pipeline that adapts per domain, per prompt, per destination |
| Wraps everything in the same verbose format | **Proportionality** — a simple prompt gets light polishing, not a 10-field schema |
| No awareness of where the prompt is going | **Destination-aware** — knows what Claude, ChatGPT, Gemini, and Perplexity can actually do |
| Blindly trusts the LLM output | **Quality verification** — automated checks catch hallucinated details and formatting leaks |
| Makes up specific numbers and presents them as yours | **Assumption transparency** — every filled-in detail gets flagged so you never send someone else's guess as your fact |
| Treats a poem the same as a business report | **Creative intelligence** — stories get *direction*, not scaffolding |

---

## Supported Platforms

<p>
  <img src="https://img.shields.io/badge/Claude-claude.ai-D97706?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude" />
  <img src="https://img.shields.io/badge/ChatGPT-chatgpt.com-10A37F?style=for-the-badge&logo=openai&logoColor=white" alt="ChatGPT" />
  <img src="https://img.shields.io/badge/Gemini-gemini.google.com-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Gemini" />
  <img src="https://img.shields.io/badge/Perplexity-perplexity.ai-1A1A2E?style=for-the-badge" alt="Perplexity" />
</p>

Keen injects natively into each platform's chat interface — no copy-pasting between tabs.

---

## Features

- ✨ **One-click enhance** — button appears natively next to each platform's send button
- ⌨️ **Keyboard shortcut** — `Ctrl+Shift+E` (or `Cmd+Shift+E` on Mac) to enhance instantly
- 🎯 **Domain-aware** — recognizes career, coding, business, creative, and more — and adjusts its approach for each
- 🧠 **Smart dosing** — measures how well-specified your prompt already is before deciding what to add
- 🛡️ **Assumption flags** — anything the enhancer fills in on your behalf is clearly marked for you to verify
- 🌙 **Dark mode aware** — UI adapts to each platform's theme
- ⚙️ **Minimal mode** — shrinks the button to a tiny icon for a cleaner interface
- 📋 **Manual mode** — paste any prompt into the popup for enhancement, even on non-supported sites

---

## How It Works

1. **You type a prompt** on any supported AI platform
2. **Click ✨ Enhance** (or press `Ctrl+Shift+E`)
3. Keen's pipeline analyzes your prompt, determines the domain and complexity, and produces an expert-level rewrite
4. **Review the result** — any assumptions are flagged with `[VERIFY: ...]` markers
5. **Send it** — the enhanced prompt stays in the composer, ready to go

The enhancement runs through a proprietary multi-stage pipeline. It's not a simple template — it classifies, retrieves domain knowledge, composes, enhances, and verifies the output, all in under 3 seconds.

---

## Before & After

**You type:**
> help me negotiate my salary

**Keen produces something like:**
> Act as a compensation strategist who judges negotiation plans by whether they include specific leverage points, a walk-away number, and a script for the actual conversation — not by how confident they sound.
>
> I need to negotiate my salary for [VERIFY: "current/incoming role" — confirm or replace].
>
> Deliver:
> 1. **Preparation framework** — what to research before the conversation
> 2. **Opening script** — exact words for the first 60 seconds
> 3. **Objection responses** — for "budget is fixed" and "we can revisit in 6 months"
> 4. **Walk-away criteria** — how to know when to stop
>
> No generic "know your worth" advice. Every suggestion must be actionable in the actual meeting.

Notice how every assumed detail is flagged as `[VERIFY: ...]` — nothing fabricated, nothing presented as your fact.

---

## Architecture (High Level)

```
┌─────────────────────────────────────┐
│  Chrome Extension (thin client)     │
│  Captures prompt · Displays result  │
│  No API keys · No sensitive logic   │
└──────────────┬──────────────────────┘
               │  Signed HTTPS
               ▼
┌─────────────────────────────────────┐
│  Backend (private server)           │
│  Enhancement pipeline               │
│  Security enforcement               │
│  Quality verification               │
└─────────────────────────────────────┘
```

The extension is a **thin client** — it captures your text and displays results. All intelligence, API keys, and security logic live on a private backend that the extension communicates with over signed HTTPS requests.

**Security highlights:**
- API keys never touch the browser
- Every request is cryptographically signed and time-stamped
- Rate limiting with progressive abuse protection
- Locked to the official extension origin — outside callers are rejected

---

## Privacy

- Keen **does not** store your prompts
- Keen **does not** train on your data
- Keen **does not** share your prompts with third parties
- Your prompts are processed in real-time and discarded

---

## Quick Start

### Install from Chrome Web Store

Search for **"Keen — every prompt, sharper"** on the [Chrome Web Store](https://chromewebstore.google.com/detail/cdfaoncajcbfmbkbcopoghmelcjjjfhh?utm_source=item-share-cb).

### Usage

1. Open Claude, ChatGPT, Gemini, or Perplexity
2. Type your prompt as usual
3. Click **✨ Enhance** or press **Ctrl+Shift+E**
4. Review the enhanced prompt — check any `[VERIFY: ...]` flags
5. Hit send

---

## FAQ

<details>
<summary><strong>Does it work on all AI platforms?</strong></summary>
<br>
Currently supported: Claude (claude.ai), ChatGPT (chatgpt.com), Gemini (gemini.google.com), and Perplexity (perplexity.ai). More platforms are planned.
</details>

<details>
<summary><strong>Does it change my prompt automatically?</strong></summary>
<br>
No — Keen replaces the text in the composer but does <strong>not</strong> auto-submit. You always review and send manually.
</details>

<details>
<summary><strong>What are the [VERIFY: ...] markers?</strong></summary>
<br>
When Keen fills in a detail you didn't provide (a budget, a timeframe, an audience), it flags it clearly so you can confirm, change, or remove it before sending. No silent assumptions.
</details>

<details>
<summary><strong>Is my data safe?</strong></summary>
<br>
Yes. Prompts are processed in real-time and not stored. API keys live exclusively on the backend — nothing sensitive exists in the extension code.
</details>

<details>
<summary><strong>Why did my prompt not change?</strong></summary>
<br>
If your prompt is conversational ("hi", "thanks") or already well-specified, Keen intentionally leaves it alone. Over-enhancing is a bug, not a feature.
</details>

---

## Feedback & Issues

Found a bug? Have a feature request? [Open an issue](../../issues) — I'd love to hear from you.

---

<p align="center">
  <sub>Built by <a href="https://github.com/Aditya-Agrahari1">Aditya Agrahari</a></sub>
</p>
