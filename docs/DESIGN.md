# StealthEmotes — experience design

A little surprise for my brother's Rogue was the intended experience. Instead of typing an emote manually, a familiar Stealth-button press could occasionally make the character giggle, laugh, grin or do something more absurd. That interruption of an ordinary action was the joke: unpredictable, brief and personal to the character.

The chance and cooldown settings control how frequently those moments can happen. The code's default chance is 100%, but the settings allow a much rarer reaction. An unsuccessful probability roll still consumes the cooldown, which is an observed behavior rather than a confirmed original creative requirement.

The addon monitors a configured action-bar slot, not the Stealth aura or the result of casting Stealth. As a result, the intended roleplaying moment and the exact technical trigger are not identical. Watch mode helps locate the slot but prints other action presses while active. Moving the ability to a different bar or changing page may require reconfiguration.

Twelve built-in WoW emotes supply the reactions. Their client-specific output, including localized behavior, has not been retested during the documentation review. No graphical interface or new feature set has been approved through this retrospective.
