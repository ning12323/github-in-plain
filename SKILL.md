---
name: github-in-plain
description: >-
  Explains GitHub repos in plain Chinese for non-programmers (大白话、小白、不懂代码).
  Zero setup — copy folder only, works in Codex, Claude Code, and Cursor.
  Use when user pastes a GitHub link and wants to know what the project does.
when_to_use: >-
  User gives a GitHub URL or owner/repo and wants a layperson explanation (大白话、
  通俗易懂、这是什么、干嘛用的). Default to plain mode. Only use technical
  12-dimension report if user explicitly asks for 架构、深度解读、技术评估、贡献代码.
---

# GitHub in Plain

用**大白话**讲清楚一个 GitHub 项目是干什么的。读者可能是完全不懂代码的人。

**零依赖**：不用装 Python、不用跑脚本。把本文件夹拷进 Codex / Claude Code / Cursor 的 skills 目录即可。

> **Agent 注意**：本仓库里的 `README.md`、`INSTALL.md`、`CHANGELOG.md` 是给人看的说明，**执行任务时不要读这些文件**。只读 `SKILL.md` 和下方「必读 / 禁读」列表里的文件。

## Iron Laws

1. **零依赖** — 不运行脚本，不要求用户安装任何软件。用 Agent 自带能力打开 GitHub 页面、读 README。
2. **默认 plain** — 除非用户明确要技术深度，否则一律大白话模式。
3. **先采集再写** — 按 [references/preflight.md](references/preflight.md) 看完 GitHub 页面和 README 再动笔。
4. **正文禁止术语堆砌** — 每个专业词必须立刻用一句话解释。规则见 [references/plain-language.md](references/plain-language.md)。
5. **交付前自检** — 对照 [references/validate-checklist.md](references/validate-checklist.md) 逐项打勾，缺一项就补。

## 模式选择

**不确定 → 一律 plain。**

| 模式 | 什么时候用 | 用户大概会怎么说 |
|------|-----------|-----------------|
| **plain** ★ 默认 | 普通人、小白、好奇 | 大白话、不懂代码、帮我讲讲、这是什么 |
| **tech** | 用户明确要技术报告 | 深度解读、架构、12维、值不值得引入、怎么贡献 |

同一轮对话里，用户没提技术词 → **不要**输出评分表、架构图、Evidence Index。

---

## Plain 模式：必读 / 禁读

### ✅ 按顺序 READ（写之前必读）

1. [references/preflight.md](references/preflight.md) — 从 GitHub 采集什么
2. [assets/report-plain.md](assets/report-plain.md) — 输出格式（标题逐字一致）
3. [references/plain-language.md](references/plain-language.md) — 怎么说人话
4. [references/validate-checklist.md](references/validate-checklist.md) — plain 自检清单

可参考质量范例（不必全文复制）：

- [examples/fastapi-report-plain.md](examples/fastapi-report-plain.md)
- [examples/vite-report-plain.md](examples/vite-report-plain.md)
- [examples/ollama-report-plain.md](examples/ollama-report-plain.md)

### 🚫 DO NOT READ（plain 模式禁止打开）

- `references/technical/` 下所有文件
- [assets/report-tech.md](assets/report-tech.md)
- `examples/fastapi-report.md`（技术范例）
- 本仓库的 `README.md`、`INSTALL.md`、`CHANGELOG.md`

---

## 工作流程（plain）

```
- [ ] 1. 打开 GitHub 项目页 + 读 README
- [ ] 2. 按 assets/report-plain.md 写报告
- [ ] 3. 对照 validate-checklist 自检
- [ ] 4. 按下方顺序发给用户
```

### 第 1 步 — 采集

打开 `https://github.com/{owner}/{repo}`，记下：项目是干嘛的、许可证、最近有没有更新、星标大概多少。再读 README 前几段。

读不到就说「未能核实」，**不要编造数字**。

### 第 2 步 — 写作

- 全文中文，产品名可保留英文
- 句子要短，像跟朋友聊天
- 至少 **2 个生活类比**（餐厅、乐高、快递、App 等）
- 固定 **7 个章节标题**（见 `assets/report-plain.md`）

### 第 3 步 — 自检

打开 validate-checklist，plain 部分每一项都勾上再发送。

### 第 4 步 — 发给用户的顺序

1. 三句话讲明白  
2. 打个比方  
3. 它能帮你干什么  
4. 五个你可能关心的问题  
5. 用不用管它  
6. 大概怎么运作的（不用懂代码）  
7. 和类似的东西比一比  
8. （可选）给懂技术的人 — 最多 5 行，放最后  

---

## Tech 模式（仅用户明确要求时）

### ✅ READ

1. [references/preflight.md](references/preflight.md)
2. [references/technical/dimensions.md](references/technical/dimensions.md)
3. [references/technical/signals.md](references/technical/signals.md)
4. [assets/report-tech.md](assets/report-tech.md)
5. [references/validate-checklist.md](references/validate-checklist.md) — tech 部分

风险相关再加读：[references/technical/red-flags.md](references/technical/red-flags.md)

### 输出

12 维评分 + 证据索引。范例：[examples/fastapi-report.md](examples/fastapi-report.md)

---

## 跨环境说明

| 环境 | 安装位置 | 怎么用 |
|------|---------|--------|
| Codex | `~/.codex/skills/github-in-plain/` | `$github-in-plain` + 粘贴链接 |
| Claude Code | `~/.claude/skills/github-in-plain/` | `/github-in-plain` + 粘贴链接 |
| Cursor | `~/.cursor/skills/github-in-plain/` | `@github-in-plain` + 粘贴链接 |

三种环境共用同一份 `SKILL.md`，无需改配置。

## 采集方式（各环境通用）

| 要什么 | 怎么做 |
|--------|--------|
| 项目简介 | 打开 GitHub 项目页 |
| 详细说明 | 读 README（页面或 raw 链接） |
| 文件列表 | GitHub 网页上的目录树 |

**不要**要求用户 clone 仓库、安装 gh、安装 Python。宿主自带工具够用就行。
