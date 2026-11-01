# StealthEmotes — decisions and evidence

## Creative choices

The addon began as a gift for my little brother's Rogue. A random giggle or similarly funny emote on pressing the Stealth button would create a small, spontaneous roleplaying moment. **Amazin**, the original project name, is connected to him and remains an acknowledgment of that inspiration.

On revisiting the project for my portfolio in November 2026, **StealthEmotes** became the repository and project name because it describes the idea more directly. Keeping the historical addon identifiers untouched separates this documentation and repository rename from a future code migration.

## Implementation observed in the source

| Source-observed approach | Evidence | Limit of interpretation |
| --- | --- | --- |
| Watch an action-bar slot | `UseAction` wrapper | Does not confirm Stealth success or state |
| Roll a random built-in emote | Emote pool and `math.random` | Does not prove any particular observed gameplay |
| Record cooldown before the chance roll | `doStealthEmoteNow()` | No recovered rationale for this specific order |
| Persist settings account-wide | `AmazinDB` in Lua/TOC | Character-specific behavior was not implemented as separate profiles |
| Use a Lua 5.0-friendly parser | `split_cmd` | Does not establish client compatibility |
| Report rested experience | `reportRestedXP()` | Separate from the original Stealth-emote idea |

The August 2025 diff records an earlier move away from aura-based handling. That code history documents *what changed*, not the complete reasoning behind it.

## Outstanding technical questions

Version labels disagree (Lua 1.2.4; TOC 1.1.0), and TOC command notes are stale. Event handling, logout persistence, slot selection, compatibility with other wrappers, cooldown boundaries, token support and localization still need client testing. These are unverified items, not retrospective claims about past failures or approved feature requests.

## Related development history

Stealth Emotes (originally Amazin) is a playful Rogue-oriented parallel experiment created for my younger brother. The current addon has 12 fixed built-in emote tokens, configurable chance/cooldown and a watched action slot; it does not confirm Stealth, and it cannot add emote tokens through a player command. See the [comparative history of the expressive addons](EMOTE_FAMILY_HISTORY.md) for the broader source-backed chronology.
