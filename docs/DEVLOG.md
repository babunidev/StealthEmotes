# StealthEmotes — development journal

**Amazin was the original addon name. StealthEmotes is the present project and GitHub repository name.**

## 2025 — a little experiment for my brother

A Rogue's Stealth button gave me a small idea for my younger brother: what if pressing it sometimes made his character giggle or perform another ridiculous emote? The resulting addon was called **Amazin**, a name tied to him, and the goal was simply to bring a bit of unexpected roleplay to that one character. Making a tool for such a specific moment was part of the fun, and the experience encouraged me to keep creating more little tools.

The surviving commits show how the code developed, though they cannot recreate every original conversation. An [August 22 change](https://github.com/babunidev/StealthEmotes/commit/8792a2b8cffa118059dd6b62bb9c8154c9f5696b) moved away from earlier aura-oriented handling toward a watched action slot. Another [August 23 change](https://github.com/babunidev/StealthEmotes/commit/9a3ead5100f246b625093735b635ea6f14fc3809) added rested-XP reporting, while a [September 11 change](https://github.com/babunidev/StealthEmotes/commit/79c3265e3c193c08b9422e868a5e39d62e522ebf) expanded the emote pool. These commits establish code changes, not the personal reasons for each decision or who executed each step.

## October 2026 — reconstructing the project

Returning to the source meant separating what the addon was meant to feel like from what it actually monitors. The present Lua hooks an action-slot press, not confirmed Stealth. AI assistance inspected source files and selected commit history, then drafted documentation of functionality, uncertainties and outstanding compatibility checks. No game-client testing took place during that review.

## November 2026 — StealthEmotes, with Amazin remembered

The portfolio needed a more descriptive project name, so **StealthEmotes** became the GitHub repository name. Still, the old name has a place in this story: **Amazin** belongs to that small experiment made for my brother, and keeping it as an honorable mention feels right. Whether he went on to use the other tools hardly matters to why this one was enjoyable to make.

With that personal history supplied by me, AI assistance revised the project documentation from my perspective and verified the current repository identity. The original `Amazin` addon files and commands remain unchanged. No new game code or in-game tests came from this documentation update.

## 1 November 2026 — placing Amazin among the other experiments

Looking back at these early addons, I wanted this personal project for my brother to remain visible beside the Buxbrew and ROAR experiments rather than disappear into a generic feature list. My AI assistant checked the current source and compared trigger mechanics: Amazin keeps its fixed twelve-emote pool and watched-button behavior, while later Roar Guild versions allow registering more native tokens. The [family history](EMOTE_FAMILY_HISTORY.md) records those distinctions and the move toward Flourish Forever. Documentation only; no new client testing.
