Stage 1. Signing in and returning to the client

The client needs a predictable transition from guest play to an account and back. In Godot, the application controller and the Arena/Wallet network adapters share these responsibilities. The client displays server-owned state instead of inventing its own balance or shared identity.

The history records native session restoration and simpler account forms on 13 October 2026. The merged source checks saved sessions against the selected server; it does not persist passwords. When accounts change, the controller separately handles an unfinished command so an old response cannot silently apply to another game session.

The result is an explicit connection state shared by account screens, gameplay and common services. Players can return without repeating the entire setup. This describes inspected source, not a new production login test.

History reference: commit 80b63ab, 13 October 2026. Inspected scripts/app.gd and scripts/wallet_api.gd at merged snapshot d8ab27b, 21 October 2026.

[All stages](md://local/godot-devlogs-en) · [Next stage](md://local/godot-inventory-en) · [Русский](md://local/godot-account-ru)
