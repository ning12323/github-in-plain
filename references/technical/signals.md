# Signal Collection Guide

Read signals in this order. Stop when the active mode's budget is satisfied.

## Priority ladder

### Tier 1 — Intent (always)

| Signal | Paths | Extract |
|--------|-------|---------|
| Purpose | `README.md`, `README.*` | One-liner, target user, non-goals |
| License | `LICENSE`, `LICENSE.*`, `COPYING` | SPDX id, commercial implications |
| Changelog | `CHANGELOG*`, GitHub Releases | Recent changes, breaking changes |

### Tier 2 — Structure (overview+)

| Signal | Paths | Extract |
|--------|-------|---------|
| Layout | top-level dirs | Module boundaries, monorepo vs single package |
| Manifest | see ecosystem table below | Dependencies, engines, version |
| Docs index | `docs/`, `mkdocs.yml`, `docusaurus.config.*` | Doc maturity |

### Tier 3 — Architecture (deep-dive+)

| Signal | Paths | Extract |
|--------|-------|---------|
| Entry | GitHub file tree / README | Start reading here |
| Config | `config/`, `*.config.*`, `settings.*` | Runtime wiring |
| Architecture docs | `docs/architecture*`, `ADR*`, `design/` | Stated design |
| Public API | exported symbols, `lib/`, `pkg/`, `src/*/mod.rs` | Extension surface |

### Tier 4 — Operations (contributor+)

| Signal | Paths | Extract |
|--------|-------|---------|
| CI | `.github/workflows/`, `.gitlab-ci.yml`, `Jenkinsfile` | Test/lint/deploy steps |
| Dev env | `Makefile`, `justfile`, `Taskfile.*`, `docker-compose*` | Dev commands |
| Contributing | `CONTRIBUTING*`, `.github/PULL_REQUEST_TEMPLATE*` | PR flow |

### Tier 5 — Health (when evaluating adoption)

| Signal | Source | Extract |
|--------|--------|---------|
| Activity | GitHub page / commits | Commit/release cadence |
| Issues | GitHub Issues tab | Open count, responsiveness proxy |
| Security | `SECURITY.md`, Dependabot, audit CI | Supply chain posture |

## Ecosystem manifest map

| Ecosystem | Primary manifest | Lockfile |
|-----------|------------------|----------|
| Node | `package.json` | `package-lock.json`, `pnpm-lock.yaml`, `yarn.lock` |
| Python | `pyproject.toml`, `setup.py`, `requirements.txt` | `poetry.lock`, `uv.lock` |
| Go | `go.mod` | `go.sum` |
| Rust | `Cargo.toml` | `Cargo.lock` |
| Java | `pom.xml`, `build.gradle*` | (wrapper) |
| Ruby | `Gemfile` | `Gemfile.lock` |
| .NET | `*.csproj`, `Directory.Packages.props` | `packages.lock.json` |

## Entry point heuristics

Scan for files matching (case-insensitive):

```
main.{py,go,rs,ts,js,java,rb}
index.{ts,js,mjs}
lib.{rs,ex}
__init__.py (package root only)
cmd/*/main.go
src/main.*
app.{py,rb,go}
```

Prefer files referenced in manifest (`bin`, `main`, `scripts.start`) over generic matches.

## README vs code verification (deep-dive)

Pick 3 claims from README or docs architecture section. For each:

1. Quote the claim
2. Find supporting or contradicting code
3. Mark: ✅ Verified | ⚠️ Partial | ❌ Not found / contradicts

Example claims: "plugin architecture", "stateless by design", "supports X protocol".

## Sampling strategy

- **Overview**: README + manifest + CI summary + GitHub About
- **Deep-dive**: Above + 3–5 core modules (not tests, not vendored deps)
- **Contributor**: Above + run install/test commands + read CONTRIBUTING end-to-end

Do not read `node_modules/`, `vendor/`, `.git/`, or generated build output.
