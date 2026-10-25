# Godot development posts: source evidence

Inspected 25 October 2026 through local Git, without changing or launching the
client's dirty working directory. Repository identity, verified from origin:
`Wratixor/geno-dice-arena-client` on git.geno-dice.com.
Public accessibility of that repository is not asserted. Posts do not require
readers to access it or reveal private connection/session data.

Merged client main: `d8ab27bfb286f747937c51215189f7d0cf3d7038`, 21 October 2026.
Its tree matches integration `ec6db55`; no uncommitted work is used as evidence.

| Post | History | Files inspected at merged main | Claim boundary |
|---|---|---|---|
| Account | `80b63abe611f890477b30c2c463a9b0f515689c0`, 13 Oct | scripts/app.gd account/adoption/recovery; scripts/wallet_api.gd | Existing session flow, no password persistence; not a fresh production login test |
| Inventory | `725d223c5b993b13f732a3eb01e2a8082b42efe4`, 18 Oct | scenes/inventory.tscn, scripts/inventory.gd, app.gd move/capability/revision handlers | Shared view, twelve slots/six sides and server-owned moves; not device acceptance |
| Battle | `725d223`, `0eb8effdc74f3729bd2dcfdcf4bd55e3c7eac2e6`, 18 Oct | docs/UI_SCENES.md, scripts/battle_presentation.gd, battle/result/component scenes | Shared presentation, reconnect queue and component icons; no final-art/export claim |
| Settings | `acd422e20a78fa007f25dd18e1c9ed9eae426f22`, 15 Oct | scripts/locale.gd, scripts/arena_text.gd, app.gd settings, docs/LOCALIZATION.md | Saved language/audio/display, untouched identity/protocol IDs; no new publication claim |

No Godot build or runtime test was performed for these prose changes. Historical
QA records orient the audit but are not presented as tests executed in this task.
Do not infer actual Windows/Android exports or a downloadable release from a
merged source commit. No balance values, unreleased story details or credentials
are introduced.

The manifest adds four RU/EN stage pairs and two index points. Games roots gain
reciprocal index links; welcome/lore retain their prior content. Existing site
and root IDs remain. Both home translations gain a Development aspect linking
to their own index. Publication uses the existing operator content deploy path.
