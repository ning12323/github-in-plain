# Red Flags & Risk Register

Use when the user asks 值不值得用, 稳不稳定, 有没有风险, or during dimensions 8–10.

Severity: **Critical** (block adoption) | **High** | **Medium** | **Low**

## Maintenance & community

| Flag | Severity | Evidence to check |
|------|----------|-------------------|
| No commit in 12+ months | High | GitHub commits / About last updated |
| Single maintainer, no bus-factor plan | Medium | Contributors graph on GitHub |
| High open issue count, low close rate | Medium | GitHub Issues tab |
| README claims "production ready" but no releases | High | tags vs README |
| Fork of abandoned upstream | Medium | README, commit history |

## Security & supply chain

| Flag | Severity | Evidence to check |
|------|----------|-------------------|
| No lockfile for application deps | Medium | manifest map in signals.md |
| Secrets or API keys in repo history | Critical | grep patterns, `.env` committed |
| No SECURITY.md for network-facing project | Medium | file presence |
| Unpinned dependencies in CI | Low | workflow YAML |
| Deprecated crypto or known-vulnerable deps | High | CVE search if obvious |

## License & legal

| Flag | Severity | Evidence to check |
|------|----------|-------------------|
| Non-OSI license (e.g. SSPL, BSL with restrictions) | High | LICENSE text |
| GPL in library meant for proprietary embedding | High | LICENSE + use case |
| Missing license file | Critical | file absence |
| Trademark restrictions unclear | Low | README legal section |

## Technical debt signals

| Flag | Severity | Evidence to check |
|------|----------|-------------------|
| No CI | High | `.github/workflows/` absent |
| Tests exist but not in CI | Medium | workflow vs `tests/` |
| Architecture docs contradict code | Medium | deep-dive verification table |
| Giant monolith README, tiny `src/` | Low | structure vs claims |

## Risk register output format

```markdown
| Risk | Severity | Evidence | Mitigation |
|------|----------|----------|------------|
| ... | High | [E3] no CI workflows | Run tests locally before adopt; consider wrapper |
```

Always tie risks to Evidence Index IDs. Do not list generic risks without repo-specific evidence.

## Verdict interaction

| Critical flags | Suggested adopter verdict |
|----------------|---------------------------|
| 0 | Follow dimension scores |
| 1+ license/security | **Avoid** or **Evaluate only** with explicit caveat |
| 2+ maintenance | **Evaluate** — require fork or vendor plan |

Contributors may still proceed if Critical flags are documented with workarounds.
