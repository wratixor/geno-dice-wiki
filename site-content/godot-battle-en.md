Stage 3. A shared visual language for battles

Network battles and local campaigns should not feel like unrelated interfaces. Godot uses shared authored scenes for battle, inventory, rewards and results. A controller supplies snapshots and receives action signals; the scene itself does not decide command prices or send network requests.

The battle view presents resources, effects, skills and a journal. Reconnection has a separate snapshot path that resets the obsolete animation queue. Journal geometry follows viewport changes and movement of the containing scene. A common result panel distinguishes victory, defeat and draw; ratings appear only when supplied by the data.

On 18 October, button icons moved into their owning components. This addresses decoration that existed in the main application but was missing in an offline instance of the same scene. Online combat rules remain server-owned and the local session retains ownership of local saves.

History references: commits 725d223 and 0eb8eff, 18 October 2026. Inspected docs/UI_SCENES.md, scripts/battle_presentation.gd and shared scenes at d8ab27b. Source inspection does not certify a current exported build or final art.

[All stages](md://local/godot-devlogs-en) · [Previous stage](md://local/godot-inventory-en) · [Next stage](md://local/godot-settings-en) · [Русский](md://local/godot-battle-ru)
