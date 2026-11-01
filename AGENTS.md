# Development rules — StealthEmotes

**By:** Babuni

Preserve project-specific player experience and source comments. Human direction belongs to Babuni.dev; credit AI separately. Existing code is evidence of an approach, not proof of historic approval or runtime verification. Record proposed, implemented and tested separately. With material edits update README, CONCEPT, ROADMAP, CHANGELOG and docs/DEVLOG. Preserve third-party credits.

## Evidence and maintenance rules

- Read the actual branch, Lua, TOC, README and relevant dated diffs before editing. Keep source behavior, proposals and tested results separate.
- Preserve Babuni.dev as project author; identify AI drafting, analysis or code assistance separately. Preserve historical records, aliases, license terms and third-party credit.
- Never treat a comment, version label or manifest interface as proof of runtime compatibility. Never claim tests were run without recording the command, environment and outcome.
- For material changes update README, CONCEPT, ROADMAP, CHANGELOG and docs/DEVLOG, plus architecture/design/content where affected. Link evidence and retain uncertainty.
- Documentation-only work must not change Lua, TOC, tests or assets. Check the diff and all relative documentation links before publishing.

## Repository-specific constraints

- Resolve Lua v1.2.4 versus TOC v1.1.0 and stale TOC command descriptions before a release; do not silently choose a version.
- Verify 1.12 event callback conventions, login/logout persistence and logout before lazy hydration.
- Check watched-slot presses with failed casts, bar paging and another UseAction wrapper.
- Exercise 0%/100% chance, cooldown boundaries, startup uptime, reset and rested-XP edge cases.
- Validate all 12 built-in tokens and fallback behavior on intended locales; prior README compatibility claims are not test results.

## Documentation voice and proposed name

Use **Babuni** for the human identity; **babuni.dev** refers to the portfolio and development platform. Tell the creative history in Babuni's first-person voice, without starting sentences with `I` or `My`. Distinguish AI-generated code, analysis and writing from Babuni's original ideas and hands-on actions. Do not fabricate original conversations or assume that source comments prove motivation. Technical descriptions may remain neutral.

**StealthEmotes** is the proposed project name, while `amazin` is the current GitHub repository and `Amazin` remains the installed addon identity. Do not silently rename files, folders, commands or saved variables.
