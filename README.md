# ChatGPT Browser Bridge Skill

一个让 AI 助手直接向 ChatGPT 提问的 skill：通过常驻浏览器会话驱动 chatgpt.com，发问、等回复、把 GPT 的原话全文带回来。用户不再需要当传话筒。

## 为什么是浏览器，而不是 API？

截至 2026-09：GitHub Models 已下线，市面上没有"免费 + 真 GPT + 稳定"的 API。真 GPT 的免费通道只剩浏览器驱动 ChatGPT 网页版——这个 skill 就是把这套流程固化成可复用的操作手册。

## 需要什么

- 能跑浏览器任务的 AI 助手（如 Muse）
- 一个 ChatGPT 账号（免费版可用，Plus 更稳）
- 用户亲手在浏览器里登录一次（密码只过用户自己的手），登录态长期有效

## 安装

把 `SKILL.md` 放到你的 skills 目录，例如 Muse 的 `~/workspace/skills/chatgpt-browser/SKILL.md`。

## 用法

- 日常：用户说"去问 GPT……" —— 新建对话提问，把 GPT 回复全文带回
- 固定项目：把项目对话的 URL 记下来，用户说"去问 GPT <项目>……"时直接在那个 thread 里接着问，GPT 有全部上下文

## 注意事项

- 用户的问题原样转发，GPT 的回复逐字带回，不摘要
- 遵守频率限制，碰到限流就停下并告诉用户
- 偶尔弹出 Cloudflare 真人验证，转人工点一下
- OpenAI 的服务条款不鼓励自动化，请按常理低频使用

## License

MIT — 详见 LICENSE 文件。

---

## English

A skill that lets an AI assistant ask ChatGPT questions directly: it drives chatgpt.com through a persistent logged-in browser session, sends the question, waits for the reply, and brings back GPT's answer verbatim. No human relay needed.

**Why a browser, not an API?** As of 2026-09 there is no free, stable API for the real ChatGPT models (GitHub Models is retired). Driving the ChatGPT web app is the remaining free path — this skill turns that workflow into a reusable playbook.

**Requirements:** an AI assistant with browser-task support (e.g. Muse), a ChatGPT account (free works, Plus is steadier), and one manual login by the user in the browser (credentials never touch the assistant). The session persists afterwards.

**Install:** drop `SKILL.md` into your skills directory.

**License:** MIT.
