# CLAUDE.md

Internal guidance for AI assistants working in the `DigitalReef-NZ/.github` repository.

## What this repo is

Org-wide GitHub configuration and community health files for the DigitalReef-NZ organisation. It is a meta-repository — no source code, no tests, no build step. Edits are plain-text changes to Markdown and dotfiles.

## File layout

| Path | Purpose |
|---|---|
| `profile/README.md` | Rendered as the org landing page at [github.com/DigitalReef-NZ](https://github.com/DigitalReef-NZ). Public-facing narrative (mission, tools, principles). |
| `README.md` | Rendered at `github.com/DigitalReef-NZ/.github`. Org-config manifest — what this repo holds and why. |
| `SECURITY.md` | Vulnerability reporting contacts and timelines. |
| `CODEOWNERS` | Default reviewer routing (currently `@wanacode`). |
| `LICENSE` | All Rights Reserved. |
| `CHANGELOG.md` | Keep-a-changelog format, tracks changes to org-wide defaults. |
| `.gitattributes`, `.gitignore` | Repository hygiene. |

## Editing guidance

- This repo is public. Never add the names of partner organisations, iwi/hapū, customers, funders, or specific staff (beyond those already in `SECURITY.md` and the org profile).
- Never reference internal architecture, infrastructure, tech stacks, CI/CD internals, or tooling repos (`security-analysis`, `dr-monitor`, etc.) beyond what already appears in `profile/README.md`.
- Keep tone infrastructural and clipped — match the voice established in `profile/README.md`.
- Use NZ English (organisation, programme, colour).
- All edits land via feature branch and PR; `main` is protected.

## What NOT to put in this repo

- GitHub workflow files (`.github/workflows/`). This repo has no workflows to run and Dependabot configs here caused weekly CI failures during Feb–Mar 2026 (historical runs were deleted 2026-04-22 after the config itself was removed in `7fc7280`). The phantom-failure side-effect is documented in `lessons-learned.md`.
- Anything that could be interpreted as a workflow target (`action.yml` at the root, `.github/workflows/*.yml`). Dependabot scans for these even when no config is present org-wide defaults would trigger.

## Related documentation

- ReefAI tool doc: `reefai/tools/github-profile/README.md`
- Public profile source: `profile/README.md`

## Verification before merge

- [ ] Changes preserve public/IP-safe boundary (no partner names, architecture, infrastructure)
- [ ] `profile/README.md` still renders correctly at github.com/DigitalReef-NZ after changes (GitHub re-renders automatically on push to default branch)
- [ ] CHANGELOG.md updated under `[Unreleased]`
