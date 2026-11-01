# StealthEmotes

**Originally Amazin · World of Warcraft 1.12**  
**Creative direction:** Babuni

StealthEmotes began as a little project for my younger brother. His Rogue had a Stealth button, and the thought of that button occasionally making the character giggle, laugh or do something equally ridiculous appealed to me. A chance-based emote could introduce a tiny, unpredictable moment of roleplay without anyone having to type it.

Back then, the addon was called **Amazin**, a name connected to my brother. The project now lives under the more descriptive name **StealthEmotes**, but keeping Amazin as its original identity is a small acknowledgment of him. Making something for one particular character, at one particular moment, was enjoyable in its own right and encouraged me to keep experimenting with little tools.

The original addon did not detect the Stealth aura or confirm a successful Stealth cast. Instead, it watched a configured action-bar slot and sometimes played a random built-in emote when that slot was pressed. That distinction remains important when describing what the code does.

## Features

- Twelve built-in emotes: ROFL, LAUGH, GIGGLE, STARE, GRIN, SMIRK, CHUCKLE, WINK, SHUSH, SNICKER, ROAR and LICK.
- Configurable emote chance from 0–100% (default: 100%).
- Configurable cooldown from 0–60 seconds (default: 6 seconds).
- A watch mode for identifying action-bar slot numbers.
- A separate command to report rested experience.

The cooldown is consumed before the probability roll, including when no emote is played. The original action is still called after the wrapper checks its slot.

## Installation and commands

**Important:** The GitHub repository is now [StealthEmotes](https://github.com/babunidev/StealthEmotes), but the installable addon still uses its historical name **Amazin**. The Lua file, TOC, saved variables and slash command have **not** been renamed.

Place `Amazin.lua` and `Amazin.toc` in `Interface/AddOns/Amazin/`, restart the client and enable the addon. Use `/amazin watch` and press the intended action button to identify its slot, then set `/amazin slot <n>` and turn watch mode off.

| Command | Source-defined behavior |
| --- | --- |
| `/amazin slot <n>` | Saves the selected action slot |
| `/amazin watch` | Toggles slot-number reports |
| `/amazin chance <0-100>` | Sets the emote probability |
| `/amazin scd <0-60>` | Sets cooldown in seconds |
| `/amazin rexp` | Reports rested XP and rounded bubbles (capped at 30) |
| `/amazin info` | Shows current slot, chance, cooldown and emote count |
| `/amazin reset` | Clears the selected slot only |
| `/amazin save` | Copies the current settings to the saved-variable table |

## Compatibility and status

This is an original Vanilla WoW 1.12 addon, not a newly verified release. The Lua header says **1.2.4** while the committed TOC declares **1.1.0**; the TOC also advertises outdated commands. Neither mismatch has been repaired by the documentation work.

Client-side verification is still outstanding for event callbacks, saved-variable loading, action-bar paging, interaction with other `UseAction` wrappers, cooldown edges and emote localization. No in-game or automated runtime tests were performed as part of the 2026 documentation updates.

## Project documentation

- [Creative concept](CONCEPT.md) · [Experience design](docs/DESIGN.md) · [Emote content](docs/CONTENT.md)
- [Architecture](docs/ARCHITECTURE.md) · [Decisions](docs/DECISIONS.md) · [Roadmap](ROADMAP.md)
- [Development journal](docs/DEVLOG.md) · [Changelog](CHANGELOG.md)
- [AI collaboration](docs/AI_COLLABORATION.md) · [Development instructions](AGENTS.md)

The [historical README](docs/HISTORICAL_README.md) is preserved as an earlier record. Older documentation and commits remain in Git history; current source takes precedence over outdated claims about behavior or compatibility.

## Place in the action-emote family

Stealth Emotes (originally Amazin) is a playful Rogue-oriented parallel experiment created for my younger brother. The current addon has 12 fixed built-in emote tokens, configurable chance/cooldown and a watched action slot; it does not confirm Stealth, and it cannot add emote tokens through a player command. See the [source-grounded family history](docs/EMOTE_FAMILY_HISTORY.md) for the progression toward Roar Guild's editable emote registry and Flourish Forever's spellcast triggers.
