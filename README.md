# GitHub in Plain

> **Multilingual README** — choose your language below.

## Languages

| | | | |
|---|---|---|---|
| [English](#english) | [简体中文](#简体中文) | [繁體中文](#繁體中文) | [日本語](#日本語) |
| [한국어](#한국어) | [Español](#español) | [Français](#français) | [Deutsch](#deutsch) |
| [Português](#português) | [Русский](#русский) | [العربية](#العربية) | |

---

## English

**Paste a GitHub link. Get a plain-language explanation anyone can understand** — no coding background required.

### Features

- **Zero dependencies** — no Python, no scripts; copy the folder and go
- **Multi-agent** — works in Codex, Claude Code, and Cursor
- **Stable structure** — every reply uses the same 7 sections: three-sentence summary, analogy, five common questions…
- **Plain language** — jargon must be explained; no unexplained tech terms

### Install

| Agent | Path |
|-------|------|
| **Codex** | `~/.codex/skills/github-in-plain/` |
| **Claude Code** | `~/.claude/skills/github-in-plain/` |
| **Cursor** | `~/.cursor/skills/github-in-plain/` |

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

Restart your agent session after installing.

### Usage

```
Explain in plain language: https://github.com/fastapi/fastapi
```

Or invoke the skill: Codex `$github-in-plain` · Claude Code `/github-in-plain` · Cursor `@github-in-plain`

### Example outputs

| Project | Type | File |
|---------|------|------|
| FastAPI | Backend API tool | [examples/fastapi-report-plain.md](examples/fastapi-report-plain.md) |
| Vite | Frontend dev tool | [examples/vite-report-plain.md](examples/vite-report-plain.md) |
| Ollama | Local AI runtime | [examples/ollama-report-plain.md](examples/ollama-report-plain.md) |

### Requirements

| Required | Not required |
|----------|--------------|
| Codex, Claude Code, or Cursor | Python, pip, virtualenv |
| This skill folder | Any scripts |
| Access to GitHub | GitHub CLI (for plain mode) |

### Technical deep-dive (optional)

Ask for **architecture**, **deep dive**, or **12-dimension evaluation** to get a technical report. Default is always plain language.

More install details: [INSTALL.md](INSTALL.md) (for humans; agents should not read it).

**License:** MIT — [LICENSE](LICENSE)

---

## 简体中文

**粘贴 GitHub 链接，用大白话讲清楚项目是干什么的。** 不懂代码也能看懂。

### 特点

- **零依赖** — 不用装 Python，不用跑脚本，复制文件夹就行
- **多环境** — Codex、Claude Code、Cursor 都能用
- **结构稳定** — 每次输出固定 7 段：三句话、类比、五个常见问题…
- **说人话** — 专业词必须解释，禁止术语堆砌

### 安装

| 工具 | 复制到 |
|------|--------|
| **Codex** | `~/.codex/skills/github-in-plain/` |
| **Claude Code** | `~/.claude/skills/github-in-plain/` |
| **Cursor** | `~/.cursor/skills/github-in-plain/` |

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

重启 Agent 会话后使用。

### 用法

```
用大白话解释：https://github.com/fastapi/fastapi
```

或：Codex `$github-in-plain` · Claude Code `/github-in-plain` · Cursor `@github-in-plain`

### 示例输出

| 项目 | 类型 | 文件 |
|------|------|------|
| FastAPI | 后端 API 工具 | [examples/fastapi-report-plain.md](examples/fastapi-report-plain.md) |
| Vite | 前端开发工具 | [examples/vite-report-plain.md](examples/vite-report-plain.md) |
| Ollama | 本地 AI 运行 | [examples/ollama-report-plain.md](examples/ollama-report-plain.md) |

### 需要什么 / 不需要什么

| 需要 | 不需要 |
|------|--------|
| Codex、Claude Code 或 Cursor | Python、pip、虚拟环境 |
| 本文件夹 | 任何脚本 |
| 能打开 GitHub | GitHub CLI（大白话模式） |

### 技术深度报告（可选）

明确说「深度解读、架构、12 维评估」时，才会输出技术向评分报告。默认始终是大白话。

详细安装：[INSTALL.md](INSTALL.md)（给人看的，Agent 不需要读）。

**许可证：** MIT — [LICENSE](LICENSE)

---

## 繁體中文

**貼上 GitHub 連結，用白話文講清楚專案在做什麼。** 不懂程式也能看懂。

### 特點

- **零依賴** — 不用裝 Python，不用跑腳本，複製資料夾即可
- **多環境** — Codex、Claude Code、Cursor 都能用
- **結構穩定** — 每次輸出固定 7 段：三句話、類比、五個常見問題…
- **說人話** — 專業詞必須解釋，避免術語堆砌

### 安裝

| 工具 | 複製到 |
|------|--------|
| **Codex** | `~/.codex/skills/github-in-plain/` |
| **Claude Code** | `~/.claude/skills/github-in-plain/` |
| **Cursor** | `~/.cursor/skills/github-in-plain/` |

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

安裝後請重新啟動 Agent 工作階段。

### 用法

```
用白話文解釋：https://github.com/fastapi/fastapi
```

或：Codex `$github-in-plain` · Claude Code `/github-in-plain` · Cursor `@github-in-plain`

### 範例輸出

| 專案 | 類型 | 檔案 |
|------|------|------|
| FastAPI | 後端 API 工具 | [examples/fastapi-report-plain.md](examples/fastapi-report-plain.md) |
| Vite | 前端開發工具 | [examples/vite-report-plain.md](examples/vite-report-plain.md) |
| Ollama | 本地 AI 執行 | [examples/ollama-report-plain.md](examples/ollama-report-plain.md) |

**授權：** MIT — [LICENSE](LICENSE)

---

## 日本語

**GitHub リンクを貼るだけ。専門用語なしで、プロジェクトが何をするか説明します。** プログラミングの知識は不要です。

### 特徴

- **依存なし** — Python 不要、スクリプト不要、フォルダをコピーするだけ
- **マルチエージェント** — Codex、Claude Code、Cursor で動作
- **安定した構成** — 毎回同じ 7 セクション（3 文要約、たとえ話、5 つのよくある質問…）
- **やさしい日本語** — 専門用語は必ず説明

### インストール

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

| エージェント | パス |
|-------------|------|
| Codex | `~/.codex/skills/github-in-plain/` |
| Claude Code | `~/.claude/skills/github-in-plain/` |
| Cursor | `~/.cursor/skills/github-in-plain/` |

インストール後、エージェントのセッションを再起動してください。

### 使い方

```
わかりやすく説明して：https://github.com/fastapi/fastapi
```

スキル呼び出し：Codex `$github-in-plain` · Claude Code `/github-in-plain`

**ライセンス：** MIT — [LICENSE](LICENSE)

---

## 한국어

**GitHub 링크를 붙여 넣으면, 코딩을 모르는 사람도 이해할 수 있게 쉬운 말로 설명합니다.**

### 특징

- **의존성 없음** — Python 불필요, 스크립트 불필요, 폴더만 복사
- **멀티 에이전트** — Codex, Claude Code, Cursor 지원
- **안정적인 구조** — 매번 동일한 7개 섹션 출력
- **쉬운 말** — 전문 용어는 반드시 설명

### 설치

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

설치 후 에이전트 세션을 다시 시작하세요.

### 사용법

```
쉬운 말로 설명해줘: https://github.com/fastapi/fastapi
```

스킬 호출: Codex `$github-in-plain` · Claude Code `/github-in-plain`

**라이선스:** MIT — [LICENSE](LICENSE)

---

## Español

**Pega un enlace de GitHub y obtén una explicación en lenguaje sencillo** — sin necesidad de saber programar.

### Características

- **Cero dependencias** — sin Python ni scripts; solo copia la carpeta
- **Multiagente** — funciona en Codex, Claude Code y Cursor
- **Estructura estable** — siempre 7 secciones: resumen en 3 frases, analogía, cinco preguntas frecuentes…
- **Lenguaje claro** — la jerga técnica debe explicarse

### Instalación

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

Reinicia la sesión del agente después de instalar.

### Uso

```
Explícalo en lenguaje sencillo: https://github.com/fastapi/fastapi
```

Invocar skill: Codex `$github-in-plain` · Claude Code `/github-in-plain`

**Licencia:** MIT — [LICENSE](LICENSE)

---

## Français

**Collez un lien GitHub et obtenez une explication en langage simple** — aucune connaissance en programmation requise.

### Fonctionnalités

- **Zéro dépendance** — pas de Python, pas de scripts ; copiez le dossier
- **Multi-agents** — Codex, Claude Code et Cursor
- **Structure stable** — 7 sections à chaque fois : résumé en 3 phrases, analogie, cinq questions courantes…
- **Langage accessible** — le jargon doit être expliqué

### Installation

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

Redémarrez la session de l'agent après l'installation.

### Utilisation

```
Explique en langage simple : https://github.com/fastapi/fastapi
```

Skill : Codex `$github-in-plain` · Claude Code `/github-in-plain`

**Licence :** MIT — [LICENSE](LICENSE)

---

## Deutsch

**GitHub-Link einfügen — klare Erklärung in einfacher Sprache.** Keine Programmierkenntnisse nötig.

### Funktionen

- **Keine Abhängigkeiten** — kein Python, keine Skripte; Ordner kopieren genügt
- **Multi-Agent** — Codex, Claude Code und Cursor
- **Stabile Struktur** — immer 7 Abschnitte: Drei-Satz-Zusammenfassung, Analogie, fünf häufige Fragen…
- **Einfache Sprache** — Fachbegriffe müssen erklärt werden

### Installation

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

Agent-Sitzung nach der Installation neu starten.

### Nutzung

```
Erkläre in einfacher Sprache: https://github.com/fastapi/fastapi
```

Skill: Codex `$github-in-plain` · Claude Code `/github-in-plain`

**Lizenz:** MIT — [LICENSE](LICENSE)

---

## Português

**Cole um link do GitHub e receba uma explicação em linguagem simples** — sem precisar saber programar.

### Recursos

- **Zero dependências** — sem Python, sem scripts; basta copiar a pasta
- **Multi-agente** — Codex, Claude Code e Cursor
- **Estrutura estável** — sempre 7 seções: resumo em 3 frases, analogia, cinco perguntas comuns…
- **Linguagem clara** — jargão técnico deve ser explicado

### Instalação

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

Reinicie a sessão do agente após instalar.

### Uso

```
Explique em linguagem simples: https://github.com/fastapi/fastapi
```

Skill: Codex `$github-in-plain` · Claude Code `/github-in-plain`

**Licença:** MIT — [LICENSE](LICENSE)

---

## Русский

**Вставьте ссылку на GitHub — получите объяснение простым языком.** Знание программирования не требуется.

### Возможности

- **Без зависимостей** — не нужны Python и скрипты; достаточно скопировать папку
- **Несколько агентов** — Codex, Claude Code и Cursor
- **Стабильная структура** — всегда 7 разделов: три предложения, аналогия, пять частых вопросов…
- **Простой язык** — термины должны объясняться

### Установка

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

После установки перезапустите сессию агента.

### Использование

```
Объясни простым языком: https://github.com/fastapi/fastapi
```

Skill: Codex `$github-in-plain` · Claude Code `/github-in-plain`

**Лицензия:** MIT — [LICENSE](LICENSE)

---

## العربية

**الصق رابط GitHub واحصل على شرح بلغة بسيطة** — لا حاجة لخبرة برمجية.

### المميزات

- **بدون تبعيات** — لا Python ولا سكربتات؛ انسخ المجلد فقط
- **متعدد الوكلاء** — Codex و Claude Code و Cursor
- **هيكل ثابت** — 7 أقسام في كل مرة: ملخص بثلاث جمل، تشبيه، خمس أسئلة شائعة…
- **لغة واضحة** — يجب شرح المصطلحات التقنية

### التثبيت

```bash
git clone https://github.com/ning12323/github-in-plain.git ~/.codex/skills/github-in-plain
```

أعد تشغيل جلسة الوكيل بعد التثبيت.

### الاستخدام

```
اشرح بلغة بسيطة: https://github.com/fastapi/fastapi
```

Skill: Codex `$github-in-plain` · Claude Code `/github-in-plain`

**الترخيص:** MIT — [LICENSE](LICENSE)

---

## About this project

| | |
|---|---|
| **Repository** | https://github.com/ning12323/github-in-plain |
| **Skill name** | `github-in-plain` |
| **Default output** | Plain Chinese (ask for English or other languages in your prompt) |
| **Install guide** | [INSTALL.md](INSTALL.md) |
