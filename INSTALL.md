# 安装说明

给**人**看的。Agent 跑 skill 时**不需要读这个文件**。

## 你需要什么

- 一台装了 **Codex** 或 **Claude Code**（或 Cursor）的电脑
- 能上网打开 GitHub

**不需要**：Python、Node、git、GitHub CLI、虚拟环境。

## Codex

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

1. 重启 Codex  
2. 输入：`$github-in-plain 用大白话解释 https://github.com/xxx/yyy`

## Claude Code

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.claude/skills/github-in-plain
```

1. 重启 Claude Code  
2. 输入：`/github-in-plain` 然后粘贴链接

## Cursor

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.cursor/skills/github-in-plain
```

使用：`@github-in-plain` + 链接

## 文件夹名

必须是 **`github-in-plain`**，和 `SKILL.md` 里的 `name` 一致。

## 怎么知道装好了？

新开对话，说：

> 我不懂代码，帮我讲讲 https://github.com/fastapi/fastapi

如果回复里有 **「三句话讲明白」**、**「打个比方」**、**「五个你可能关心的问题」**，就说明 skill 生效了。

## 更新

```bash
cd ~/.codex/skills/github-in-plain   # 或 .claude / .cursor 路径
git pull
```

然后重启 Agent 会话。

## 常见问题

**问：要不要装 Python？**  
答：不要。整个 skill 就是 Markdown 指令，没有脚本。

**问：输出太技术怎么办？**  
答：加上「大白话」「不懂代码」「我是小白」。

**问：三种工具指令一样吗？**  
答：skill 内容一样，只是唤起方式不同（`$` / `/` / `@`）。
