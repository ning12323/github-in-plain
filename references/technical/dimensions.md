# GitHub in Plain — 12 维技术评估

Each dimension: **score 1–5**, **one-liner**, **≥1 evidence**. Use conservative scores when evidence is thin.

## Scoring rubric (global)

| Score | Meaning |
|-------|---------|
| 5 | Excellent — clear evidence, best-in-class for problem space |
| 4 | Good — minor gaps |
| 3 | Adequate — usable with caveats |
| 2 | Weak — significant gaps or concerns |
| 1 | Poor / unknown — avoid or investigate further |

---

## 1. Problem Fit

**Question**: What problem does this solve? Where are the boundaries?

| Score | Criteria |
|-------|----------|
| 5 | README + examples clearly define problem, non-goals, and target users |
| 3 | Problem stated but boundaries vague |
| 1 | Marketing fluff only; problem unclear |

**Look at**: README intro, docs positioning, examples/, comparison tables in docs.

**One-liner template**: 「解决 {pain}，面向 {user}，不适用于 {anti-pattern}」

---

## 2. Architecture

**Question**: How is the system layered? What are module boundaries and data flow?

| Score | Criteria |
|-------|----------|
| 5 | Documented architecture matches code; clear layers and boundaries |
| 3 | Inferrable from structure; docs partial or stale |
| 1 | Spaghetti or no discernible structure |

**Look at**: `src/` layout, package boundaries, `docs/architecture*`, ADRs, main entry files.

**Deep-dive**: Include mermaid diagram (components + data flow).

---

## 3. Entry Points

**Question**: Where should a reader start? What are the critical files?

| Score | Criteria |
|-------|----------|
| 5 | Obvious entry files; docs or CONTRIBUTING name them |
| 3 | Entry inferrable with effort |
| 1 | No clear starting point |

**Look at**: `main.*`, `index.*`, `__init__.py`, `cmd/`, `packages/*/src`, GitHub file tree.

**Output**: Ordered reading list (3–7 files) with `path` and why each matters.

---

## 4. Tech Stack

**Question**: Languages, frameworks, runtime — and why these choices matter.

| Score | Criteria |
|-------|----------|
| 5 | Stack clear; versions pinned; rationale documented or obvious |
| 3 | Stack clear; rationale unstated |
| 1 | Stack unclear or conflicting manifests |

**Look at**: Manifest files, `Dockerfile`, `go.mod`, `package.json`, `pyproject.toml`, `Cargo.toml`, CI matrix.

---

## 5. Extensibility

**Question**: How do users extend, plugin, or integrate?

| Score | Criteria |
|-------|----------|
| 5 | Plugin API, hooks, or extension docs with examples |
| 3 | Extension via config or subclassing; docs sparse |
| 1 | Closed system; fork required for customization |

**Look at**: `plugin*`, `extension*`, middleware hooks, public API surface, `examples/custom*`.

---

## 6. Ops Reality

**Question**: How do you run, test, deploy? What resources are needed?

| Score | Criteria |
|-------|----------|
| 5 | One-command dev setup; Docker/k8s; docs match CI |
| 3 | Setup documented but multi-step or fragile |
| 1 | Cannot run without tribal knowledge |

**Look at**: README install, `Makefile`, `docker-compose*`, CI install steps, `scripts/`.

**Contributor mode**: Paste exact commands you would run (clone → install → test).

---

## 7. Quality Signals

**Question**: Tests, CI, lint, coverage — is quality enforced?

| Score | Criteria |
|-------|----------|
| 5 | CI runs tests + lint; coverage reported; pre-commit hooks |
| 3 | CI exists; tests partial |
| 1 | No CI or tests |

**Look at**: `.github/workflows/`, `tests/`, `*_test.*`, `.pre-commit-config.yaml`, codecov badges.

---

## 8. Security & Supply Chain

**Question**: Dependency risk, security tooling, sensitive patterns?

| Score | Criteria |
|-------|----------|
| 5 | Dependabot/Renovate, security policy, audit in CI |
| 3 | Lockfile present; no explicit security process |
| 1 | No lockfile; known risky patterns |

**Look at**: `SECURITY.md`, Dependabot config, lockfiles, `npm audit` / `cargo audit` in CI, secrets in repo.

See also [red-flags.md](red-flags.md).

---

## 9. Community Health

**Question**: Is the project alive? Who maintains it?

| Score | Criteria |
|-------|----------|
| 5 | Active commits, responsive issues, diverse contributors |
| 3 | Maintained but slow; small core team |
| 1 | Stale (>12mo no release), single maintainer risk, ignored issues |

**Look at**: GitHub About / activity, contributor graph, issue close rate, bus factor hints.

---

## 10. Release & Stability

**Question**: Versioning, breaking changes, migration path?

| Score | Criteria |
|-------|----------|
| 5 | Semver, CHANGELOG, migration guides, predictable cadence |
| 3 | Releases exist; breaking changes poorly documented |
| 1 | No releases or chaotic versioning |

**Look at**: Tags, GitHub Releases, CHANGELOG, `BREAKING` notes, deprecation policy.

---

## 11. License & Governance

**Question**: Can you use it commercially? Fork? Who decides direction?

| Score | Criteria |
|-------|----------|
| 5 | OSI license, CLA/DCO clear, governance doc if foundation |
| 3 | Standard license; governance informal |
| 1 | Custom/restrictive license or unclear ownership |

**Look at**: LICENSE, `CLA.md`, DCO, trademark notes, foundation docs (CNCF, Apache, etc.).

---

## 12. Positioning

**Question**: vs alternatives — when to pick this vs others?

| Score | Criteria |
|-------|----------|
| 5 | Explicit comparison or clear niche; you can articulate tradeoffs |
| 3 | Niche inferrable; user must compare manually |
| 1 | Redundant with better-known tools; no differentiation |

**Output**: Table comparing 2–3 peers on: problem fit, complexity, ecosystem, license, maturity.

If user named competitors, include them. Otherwise pick peers from same problem space.
