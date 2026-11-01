# StealthEmotes — concept

**By:** Babuni

I wanted a stealth-themed character reaction tied to an action-bar button. The current addon watches one configured action-bar slot. Pressing that slot may play a random built-in emote after a cooldown, then delegates to the original action. It does not detect successful Stealth casts or actual stealth state. A separate command reports rested XP.

The small interaction gives a stealth-themed action a comic character reaction. This description comes from the current code and historical README. My complete original development conversation has not been recovered, so the reasons behind every iteration remain uncertain. Slot watching avoids dependence on aura/icon detection, but pressing the slot is not proof that Stealth succeeded. Moving or paging action bars can change what the selected slot means.

Chance and cooldown offer two independent controls over frequency. Watch mode helps discover slot numbers, but prints every action while enabled. The addon wraps a global function, so other action-bar addons and load order need a combined test. Historical claims that it works on every locale remain unverified in this pass.

## Evidence and status

Reviewed on 2026-10-26 against `main` at [e96070a](https://github.com/babunidev/amazin/commit/e96070a7cf16ed4605caafaf018a566f74d63207). Current Lua, TOC, README and dated commit history were inspected. Source describes implementation; it does not establish successful operation. Historical intent is reconstructed only where labeled. No in-client test or automated test was executed during this documentation pass.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# StealthEmotes — concept

**By:** Babuni

A Vanilla 1.12 stealth-themed emote addon with cooldown, random chance, watched action slot and rested-experience reporting.

## Design visible in the repository

Stealth is inferred from the watched button rather than a buff/icon, which avoids fragile client aura checks.

This concept is reconstructed from README.md, the main addon Lua file and the .toc manifest; the idea and creative direction belong to me, Babuni. No unrecorded decisions are invented.
