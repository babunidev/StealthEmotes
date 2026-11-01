# Development instructions — StealthEmotes

**Human creative and project author:** Babuni  
**Portfolio:** babuni.dev

## Authorship and voice

The original idea was a small, chance-based roleplay addon for Babuni's younger brother's Rogue. It was called **Amazin** in connection with him; **StealthEmotes** is the current repository/project name. Preserve that personal origin without inventing the brother's actual name, a usage history or motivations for every technical change.

Write public-facing histories from Babuni's first-person perspective. Never begin a sentence with **I** or **My**. Use **creative** as the role label for the human who conceived the work. Keep the narrative concise and relatable; do not present the creative in the third person within their own story. Technical reference documents may be neutral.

Credit AI for the research, drafting, coding or other work it actually performed. Do not ascribe Babuni's ideas to AI, or imply Babuni manually wrote code produced by AI. Distinguish proposed, implemented and tested actions.

## Identity and compatibility

- Repository: `babunidev/StealthEmotes`.
- Original installed addon: `Amazin`, with `Amazin.lua`, `Amazin.toc`, `/amazin` and `AmazinDB`.
- The project rename does **not** authorize renaming runtime identifiers. Any migration requires an explicit decision and compatibility plan.
- The code watches a selected action slot; never describe this as detecting successful Stealth or the Stealth aura.
- Lua version 1.2.4 and TOC version 1.1.0 conflict. Command notes in the TOC are outdated. Do not silently resolve either.

## Maintenance rules

- Inspect the current source and relevant commit evidence before describing functionality or proposing changes.
- Keep personal recollection, source-backed observations, historical inference and verified test results distinct.
- Preserve earlier commits and the verbatim `docs/HISTORICAL_README.md`; do not rewrite history to imply unrecorded certainty.
- With substantial changes, update README, CONCEPT, ROADMAP, CHANGELOG and docs/DEVLOG; update architectural, design and attribution notes where relevant.
- Keep documentation-only changes separate from game code. Test and report any code changes against the intended client when possible.
- Check paths, links, compatibility claims and the final diff before committing.

## Verification priorities

Verify WoW 1.12 event callbacks, login/logout settings persistence, slot paging and failed-cast behavior, coexistence with other `UseAction` hooks, initial cooldown timing, chance extremes, all emote tokens, locales and rested-XP boundaries. Do not call these checks completed until results exist.
