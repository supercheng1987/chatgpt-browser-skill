# ChatGPT Browser Bridge Skill

[中文版](README.md)

**The problem it solves:** You build projects with ChatGPT (code, plans, brainstorming) and you also use Muse as your AI assistant. Before, every message between the two went through you via copy-paste — this skill lets Muse log into your ChatGPT account directly, ask questions, and bring back GPT's answers verbatim. You stop being the relay.

## Who is this for?

- You have ongoing projects in ChatGPT (code or plans you built together with GPT) that you want to move over to Muse or have Muse join in on
- You use Muse (Meta AI) as your assistant and want it to talk to GPT directly
- Honestly: you need both sides. If you only use ChatGPT and don't have an AI assistant, this skill isn't for you.

## How it works

Muse drives chatgpt.com through a persistent browser task logged into your ChatGPT account (you log in once by hand — credentials never touch the assistant — and the session persists). You say "ask GPT…", Muse opens a new conversation (or your specified project thread, so GPT has the full context), asks the question, waits for streaming to finish, and brings back the full reply word for word.

## Requirements

- A ChatGPT account (free tier works; Plus is steadier)
- An AI assistant with browser-task support, e.g. Muse
- One manual login to ChatGPT in the browser, done by you

## Install

Drop `SKILL.md` into your skills directory, e.g. `~/workspace/skills/chatgpt-browser/SKILL.md` for Muse.

## Usage

- Everyday: you say "ask GPT…" — Muse starts a new conversation, asks, and brings back the full reply
- Project threads: save the URL of your ChatGPT project conversation; say "ask GPT about \<project\>…" and Muse continues in that thread with full context — no need for you to re-explain the background

## Notes

- Your question is forwarded verbatim; GPT's reply comes back word for word — never summarized
- Respect rate limits; if throttled, stop and tell the user
- A Cloudflare "verify you are human" challenge may occasionally pop up — hand control to the user to click through
- OpenAI's terms discourage automation; keep usage reasonable and low-frequency

## License

MIT — see the LICENSE file.
