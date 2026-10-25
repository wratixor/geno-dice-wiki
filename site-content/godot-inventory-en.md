Stage 2. Inventory as a shared screen

The inventory must explain what a die contains and what dragging a face will do. The current shared screen presents twelve slots, six assigned sides, a die radar and selected-face details. Its scene emits selection, movement, fusion, absorption and deletion signals to the owning controller.

In network play, the server confirms slot order. The client checks inventory_reorder_v1 before moving a face and sends the expected revision. An unsupported operation cannot masquerade as a saved local rearrangement. Offline campaigns use the same screen while their local session owns mutations and saves.

Shared confirmations let players cancel destructive actions; suppressing a repeated prompt is saved only after confirmation. Separating the scene from its controller lets presentation change without mixing online account authority with local campaign rules.

History reference: commit 725d223, 18 October 2026, extracts shared scenes. Inspected scenes/inventory.tscn, scripts/inventory.gd and the move handler in scripts/app.gd at d8ab27b. This is not a new physical-device test.

[All stages](md://local/godot-devlogs-en) · [Previous stage](md://local/godot-account-en) · [Next stage](md://local/godot-battle-en) · [Русский](md://local/godot-inventory-ru)
