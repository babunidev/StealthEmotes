# StealthEmotes — roadmap

**Creative direction:** Babuni

The original goal was a small, chance-based Rogue emote addon for my little brother, not an ongoing product roadmap. The repository has since been renamed **StealthEmotes**; the installed addon remains **Amazin**.

## Existing source

- One configurable watched action-bar slot.
- Twelve built-in emotes with chance and cooldown settings.
- Watch mode and rested-XP reporting.
- Account-wide saved-variable table `AmazinDB`.

These features are present in source, not newly certified by a game-client test.

## Unverified technical work

- [ ] Reconcile the Lua 1.2.4 and TOC 1.1.0 version labels and outdated manifest command descriptions.
- [ ] Verify WoW 1.12 event callbacks and persistence, including logout before settings load.
- [ ] Test failed casts, action-bar paging and coexistence with another `UseAction` wrapper.
- [ ] Test chance limits, cooldown limits and initial cooldown behavior.
- [ ] Verify all built-in emote tokens, localization and rested-XP edge cases.

These are verification tasks, **not approved feature additions**. No new gameplay functionality or release has been planned as part of the documentation rewrite.

## Related development history

Stealth Emotes (originally Amazin) is a playful Rogue-oriented parallel experiment created for my younger brother. The current addon has 12 fixed built-in emote tokens, configurable chance/cooldown and a watched action slot; it does not confirm Stealth, and it cannot add emote tokens through a player command. See the [comparative history of the expressive addons](docs/EMOTE_FAMILY_HISTORY.md) for the broader source-backed chronology.
