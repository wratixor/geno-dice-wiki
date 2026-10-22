# Geno-Dice Wiki content

Public Markdown roots for [Geno-Dice Wiki](https://wiki.geno-dice.com/).
The application and shared database belong to the existing
[NODE06 service](https://github.com/wratixor/node06). This repository contains
content only; it does not deploy a second server or database.

Registered entry: `s_ab283767530445ab9abb091eb7d192bb`.

Self-service Git import is still being implemented in NODE06. An operator
publication path is prepared in NODE06 and geno-dice-deploy; it requires reviewed
application/toolkit updates and an explicit content binding on the existing
server. Committing here changes the live wiki only after an operator release
with that binding enabled. No deployment has been verified by this repository. See NODE06 `docs/ROOT-PREFLIGHT-V1.md`
for the implemented read-only validation contract.

## Editing and validation

`node06-roots.json` opts in only the files under `site-content/`. The bilingual
welcome connects four independent starter points. These are navigation stubs,
not a complete game manual or a publication of internal lore. There are no
language-specific routes. Add source-verified public material incrementally.

From an existing NODE06 checkout, use its installed backend environment:

```sh
python -m node06_service.root_preflight --repo /path/to/geno-dice-wiki \
  --commit FULL_40_CHARACTER_COMMIT_SHA \
  --site-id s_ab283767530445ab9abb091eb7d192bb
```

Preflight does not prove ownership or write to the database. The operator
release selects this public repository in root-owned `node06-content.conf` and
publishes the reviewed main SHA into the existing registered site. The application
records operator authority, source provenance and immutable point revisions.
This route does not need another site registration or a fabricated source proof.
A future self-service source registration will issue a real proof, followed by
preview and explicit acceptance. `welcome.mode=git` describes the proposed import; it does
not switch the current UI-managed welcome by itself; an accepted operator
publication explicitly switches it to Git management. Keep the existing site registration.
The Neocities entry has its own ID and may use a different content repository.

No engine code or workflows are copied here. GitHub Actions is disabled for
this repository. Code licensing upstream does not grant a new content license;
content licensing remains an owner decision.


## Repository-owned home page

`home_page` in `node06-roots.json` defines the landing title, introduction and
aspect blocks. `point_id: "local/games-ru"` refers to a declared root in this
manifest; `local/welcome` refers to the existing site entrance. Public global IDs
or HTTP(S) external URLs are also supported. These navigation links do not create
graph relations. The two starter blocks are Games and World, not language routes.

Release order: merge the NODE06 Git-home feature (migration 0007) to application
main before merging this content update; then run the ordinary explicit NODE06
deploy. Older applications reject the new manifest field rather than executing it.
Do not merge content first and deploy with an older application main. Repository
files/scripts/HTML are never run by the content publisher.

New sites default to automatic priority: accepted Git home, then site settings,
then welcome. Existing saved UI layouts retain their choice on migration. In
`/sites/` the owner can select Auto, Git, site settings or welcome; Git publication
does not erase the saved UI layout or force the owner's selection. Removing the
manifest home clears its accepted Git snapshot at the next successful release;
temporary fetch/validation failure preserves the last accepted snapshot.
