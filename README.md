# ChatGPT Browser Bridge Skill

[English version](README_EN.md)

**解决一个具体麻烦：** 你在 ChatGPT 里做项目（写代码、聊方案），同时用 Muse 当 AI 助手。以前两边传话全靠你复制粘贴——这个 skill 让 Muse 直接登录你的 ChatGPT 账号去提问，把 GPT 的原话全文带回来。你不再当传话筒。

## 这是谁用的？

- 你在 ChatGPT 里有正在进行的项目（比如和 GPT 一起写的代码、方案），想转到 Muse 这边或让 Muse 参与进去
- 你同时用 Muse（Meta AI）当助手，希望它能直接跟 GPT 对话
- 说实话：两边都得有。只用 ChatGPT、没有 AI 助手的人用不上这个 skill

## 它是怎么工作的？

Muse 通过一个常驻浏览器任务登录你的 ChatGPT 账号（你亲手登一次，密码只过你自己的手，登录态长期有效）。你说"去问 GPT……"，Muse 就去 chatgpt.com 新建对话（或打开你指定的项目对话，GPT 有全部上下文）提问，等回复流式结束，把全文逐字带回来。

## 需要什么

- 一个 ChatGPT 账号（免费版可用，Plus 更稳）
- 能跑浏览器任务的 AI 助手，比如 Muse
- 你亲手在浏览器里登录一次 ChatGPT

## 安装

把 `SKILL.md` 放到你的 skills 目录，例如 Muse 的 `~/workspace/skills/chatgpt-browser/SKILL.md`。

## 用法

- 日常：你说"去问 GPT……" —— Muse 新建对话提问，把 GPT 回复全文带回
- 项目对话：把你在 ChatGPT 里的项目对话 URL 记下来，说"去问 GPT <项目>……"时 Muse 直接在那个 thread 里接着问，GPT 有全部上下文，不用你转述背景

## 注意事项

- 你的问题原样转发，GPT 的回复逐字带回，不摘要
- 遵守频率限制，碰到限流就停下并告诉你
- 偶尔弹出 Cloudflare 真人验证，转人工点一下
- OpenAI 的服务条款不鼓励自动化，请按常理低频使用

## License

MIT — 详见 LICENSE 文件。
