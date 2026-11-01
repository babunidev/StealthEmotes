# StealthEmotes — architecture

The original addon ships as `Amazin.lua` and `Amazin.toc` for WoW 1.12. This document describes the current source, not a verified runtime test.

## Action interception

The Lua file captures `UseAction` in `_Orig_UseAction` and replaces the global function with a wrapper. Each invocation calls `ensureLoaded()`, optionally prints the pressed slot in watch mode, checks whether it matches `WATCH_SLOT`, and finally invokes the original action with its original arguments.

A matching press is **not** proof that Stealth succeeded. Action-bar paging, failed casts, or other addons wrapping `UseAction` can affect the observable behavior.

## Emote selection and cooldown

`doStealthEmoteNow()` compares `GetTime()` with `LAST_STEALTH_EMOTE_TIME`. Once the cooldown permits an attempt, the timestamp is updated **before** the random chance roll; a failed roll therefore consumes cooldown. A successful roll selects one of twelve built-in tokens with `math.random` and calls `DoEmote`. If `DoEmote` is unavailable, the implementation sends the fixed German fallback text `kichert leise...` as an EMOTE.

`LAST_STEALTH_EMOTE_TIME` starts at zero, so first-use eligibility can depend on uptime. The default cooldown is six seconds, default chance 100%.

## Settings and events

`AmazinDB` is an account-wide saved-variable table containing `slot`, `stealth_chance` and `stealth_cd`. Settings hydrate lazily when a slash command or action invocation calls `ensureLoaded()`. Watch mode and last-emote timestamp are not persisted.

The file registers `PLAYER_LOGIN` to seed the random generator and `PLAYER_LOGOUT` to copy settings to the saved-variable table. Callback conventions for the target WoW 1.12 runtime and logout before lazy hydration require verification.

## Additional command

`/amazin rexp` reads rested XP and the player's maximum XP, calculates rounded rested-XP bubbles via `floor(restedXP * 20 / maxXP + 0.5)`, then caps the result at 30. Missing data has a local chat message rather than a crash path.

## Known discrepancies

Lua identifies version **1.2.4** while the TOC says **1.1.0** and contains obsolete command descriptions. The repository rename to **StealthEmotes** does not change the addon package or these identifiers. No automated test suite or new in-game verification is recorded for this documentation revision.
