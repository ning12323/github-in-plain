# GitHub in Plain

**粘贴 GitHub 链接，用大白话讲清楚项目是干什么的。** 不懂代码也能看懂。

## 特点

- **零依赖** — 不用装 Python，不用跑脚本，复制文件夹就行
- **多环境** — Codex、Claude Code、Cursor 都能用
- **结构稳定** — 每次输出固定 7 段：三句话、类比、五个常见问题…
- **说人话** — 专业词必须解释，禁止术语堆砌

## 安装（三选一）

| 工具 | 复制到 |
|------|--------|
| **Codex** | `~/.codex/skills/github-in-plain/` |
| **Claude Code** | `~/.claude/skills/github-in-plain/` |
| **Cursor** | `~/.cursor/skills/github-in-plain/` |

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

重启 Agent 会话后使用。

## 怎么用

```
用大白话解释：https://github.com/fastapi/fastapi
```

或（Codex）`$github-in-plain` ·（Claude Code）`/github-in-plain`

## 示例输出

| 项目 | 类型 | 文件 |
|------|------|------|
| FastAPI | 后端 API 工具 | [examples/fastapi-report-plain.md](examples/fastapi-report-plain.md) |
| Vite | 前端开发工具 | [examples/vite-report-plain.md](examples/vite-report-plain.md) |
| Ollama | 本地 AI 运行 | [examples/ollama-report-plain.md](examples/ollama-report-plain.md) |

## 需要什么 / 不需要什么

| 需要 | 不需要 |
|------|--------|
| Codex 或 Claude Code 或 Cursor | Python、pip、虚拟环境 |
| 本文件夹 | 任何脚本 |
| 能打开 GitHub | git clone、GitHub CLI |

## 技术深度报告（可选）

明确说「深度解读、架构、12 维评估」时，才会输出技术向评分报告。默认始终是大白话。

## 详细安装说明

见 [INSTALL.md](INSTALL.md)（给人看的，Agent 执行 skill 时不需要读）。

## License

MIT — [LICENSE](LICENSE)
