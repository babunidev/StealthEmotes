# StealthEmotes — concept

**Creative direction:** Babuni

## Why this exists

A small gift for my little brother was the starting point. The idea was to give his Rogue a few unexpected roleplaying reactions: press the Stealth button, and occasionally the character might giggle, laugh or make another funny emote. The randomness mattered. A reaction on every press would become mechanical; a surprise now and then could feel like the character had a mischievous streak.

The original name, **Amazin**, honored that personal connection. Later, when revisiting the project for my portfolio, **StealthEmotes** became the clearer name for what it was designed around. Amazin remains part of the history rather than disappearing with the repository rename.

## How the concept became an addon

The code monitors one selected action-bar slot, not a stealth-state change. It wraps WoW's `UseAction` function, checks whether the pressed slot matches the configured one, applies a cooldown and random chance, then passes control to the original action. The emotes are built-in game commands, not custom animations. A separate `/amazin rexp` command reports rested experience.

A 2025 commit shows a shift away from earlier aura-related logic toward slot monitoring. The exact reasons for each internal implementation decision are not recoverable from the commit alone. The personal purpose described above comes from my own account of why the addon was made, not from a speculative reading of code.

## Scope

This was made for one character and one playful experience, not conceived as a general roleplaying framework. Later features and code revisions can be documented on their own terms without turning that original moment into a larger plan that did not exist.

**Status:** The design and existing source have been reviewed retrospectively; no renewed in-game verification has been performed.

## Related development history

Stealth Emotes (originally Amazin) is a playful Rogue-oriented parallel experiment created for my younger brother. The current addon has 12 fixed built-in emote tokens, configurable chance/cooldown and a watched action slot; it does not confirm Stealth, and it cannot add emote tokens through a player command. See the [comparative history of the expressive addons](docs/EMOTE_FAMILY_HISTORY.md) for the broader source-backed chronology.
