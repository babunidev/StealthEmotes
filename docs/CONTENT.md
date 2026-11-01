# StealthEmotes — content inventory

The character reactions use twelve built-in World of Warcraft emote tokens:

`ROFL`, `LAUGH`, `GIGGLE`, `STARE`, `GRIN`, `SMIRK`, `CHUCKLE`, `WINK`, `SHUSH`, `SNICKER`, `ROAR`, `LICK`.

The older README listed ten. A September 2025 source commit added `ROAR` and `LICK`. These are game-provided emotes, not original animations or art assets.

The fixed fallback text is `kichert leise...`, sent as an EMOTE when `DoEmote` is missing. Other source strings include the `Amazin:` chat prefix, slot reports, setting confirmations, command help and rested-XP messages. `/amazin rexp` rounds rested XP to bubbles and caps the display at 30.

The original creative aim was a comical, occasionally surprising reaction for a younger brother's Rogue. The current emote list is source-verified, but the availability and localized output of every token have not been tested during the 2026 documentation work.
