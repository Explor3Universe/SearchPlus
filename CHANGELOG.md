# Changelog

All notable changes to this project are documented in this file. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and versions follow [Semantic Versioning](https://semver.org/).

## [1.1.1] — 2026-11-19

### Added

- Plugin icon (`assets/icon.png`), referenced from the Claude Code, Cursor and Agent Plugins manifests.
- Cursor plugin manifest (`.cursor-plugin/plugin.json`).

## [1.1.0] — 2026-11-19

### Changed

- The skill moved from `searchplus/` to `skills/searchplus/`, the standard location other agents and catalogs look in.

### Added

- A portable `plugin.json` (Agent Plugins format), read by Codex and Antigravity.
- `gemini-extension.json`: SearchPlus installs as a Gemini CLI extension.
- README: install instructions for Codex, Gemini CLI and other agents via `npx skills`.
- README in Ukrainian and Hebrew.

## [1.0.0] — 2026-11-19

First release.

### Added

- The `searchplus` skill in English:
  - the core: seven steps that are never cut;
  - Law 0, the self-refutation duel: death and cause queries, the state owner and its layers, evidence binding, symmetric weighing and three verdicts;
  - Laws 1–3: query saturation, reformulation and the language matrix;
  - the research cycle, stop conditions, the answer standard and a 10-item pre-send checklist.
- References: `verification.md`, `query-arsenal.md`, `languages.md`, `verticals.md`, `log-template.md`.
- Claude Code plugin manifest and marketplace in `.claude-plugin/`: one-command install.
- An eval suite for `claude plugin eval` in `evals/`: 9 trigger cases and 9 behavior cases built from real test questions.
- README in English and Russian.
- License: Apache-2.0.

[1.1.1]: https://github.com/Explor3Universe/SearchPlus/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/Explor3Universe/SearchPlus/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/Explor3Universe/SearchPlus/releases/tag/v1.0.0
