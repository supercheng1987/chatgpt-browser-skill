---
name: chatgpt-browser
description: Ask ChatGPT (GPT) questions through a persistent logged-in browser session and bring back answers verbatim. Use when the user says "ask GPT…" or wants GPT's input without relaying messages themselves.
---

# ChatGPT Browser Bridge

There is no free, stable API for the real ChatGPT models (as of 2026-09), so this skill drives chatgpt.com through a live browser task to ask GPT questions on the user's behalf — no relaying needed.

## Prerequisites

- The browser profile must be logged into the user's ChatGPT account. The user logs in once by taking over the browser window; the session then persists.
- Never ask the user for their password in chat. Sign-in is always completed by the user's own hand.

## Standard flow (browser.spawn_task)

Task template:

```
Open https://chatgpt.com/ and confirm you are logged in (chat input box visible).
Start a new conversation and send the following message to GPT verbatim:

<the user's question, word for word>

Wait until GPT's reply has fully finished streaming, then record the complete
reply text word for word and report it together with the conversation URL.
Do not log out. Do not open other conversations from history.
```

## Project-specific threads (optional)

If the user regularly discusses a specific project with GPT, keep that conversation's URL in your own notes. When the user names the project, continue that thread (open the URL directly) so GPT has the full context instead of starting fresh.

## Rules

- Forward the user's question **verbatim** — never rewrite or embellish it.
- Bring back GPT's reply **in full, word for word** — never summarize. Summarizing is the user's decision.
- One question per task; to continue a thread, steer the same browser task.
- Respect rate limits (free and Plus accounts both throttle): don't fire messages in rapid succession; if throttled, stop and tell the user.
- A Cloudflare "verify you are human" challenge may occasionally appear: hand control to the user to click through it.
- Never request passwords or one-time codes in chat; sign-in steps are always completed by the user in the browser.
