Stage 4. Language and settings without losing progress

Changing language must not change a die, a player name or campaign progress. Persistent Russian/English selection was added on 15 October. It lives in device settings, uses the standard TranslationServer and treats dynamic UI strings separately from authored content fields.

ArenaText translates labels for display. Player names and renamed dice remain user data; protocol IDs and file names are not translated. Dialogues use separate language fields, so changing language does not rewrite the source text in a save.

The same settings file stores music/effect volumes, mute and reduced motion. Settings updates load the previous file before changing selected fields, preserving other options. Language selection is loaded at startup; an absent or invalid saved choice falls back to the system language.

History reference: commit acd422e, 15 October 2026. Inspected scripts/locale.gd, scripts/arena_text.gd, settings handlers and docs/LOCALIZATION.md at d8ab27b. This verifies source structure, not a new client publication.

[All stages](md://local/godot-devlogs-en) · [Previous stage](md://local/godot-battle-en) · [Русский](md://local/godot-settings-ru)
