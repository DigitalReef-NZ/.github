# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Added

- `CLAUDE.md` — internal editing guidance for AI assistants working in this repo.
- `README.md` expanded from stub to org-config manifest with file inventory, links to org profile, and security/contribution pointers (`e68e821`, 2026-04-22).

### Removed

- `.github/dependabot.yml` — Dependabot was configured to scan `github_actions` but this repo has no workflows, causing nine consecutive weekly CI failures (2026-02-11 through 2026-03-31). Config removed in `7fc7280` (2026-04-02). Historical failed runs cleared 2026-04-22 to resolve phantom-failure signal in org-wide CI Health monitoring.

### Fixed

- `CODEOWNERS` default reviewer set to `@wanacode` (`b15facb`, pre-session).
