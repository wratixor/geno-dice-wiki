# Geno-Dice Wiki content

Public Markdown roots for [Geno-Dice Wiki](https://wiki.geno-dice.com/).
The application and shared database belong to the existing
[NODE06 service](https://github.com/wratixor/node06). This repository contains
content only; it does not deploy a second server or database.

Registered entry: `s_ab283767530445ab9abb091eb7d192bb`.

The existing server's operator content binding and NODE06 deploy scripts select
this repository's reviewed main commit. The configured deployment timer can pick
up a merged content update; committing or pushing a feature branch is not a live
publication. Keep that binding and the existing registration. No new server,
site registration, source proof or workflow is needed for this change.

NODE06 also implements owner-managed public GitHub sources with proof,
preview/accept and optional polling (`docs/GIT-SOURCES-V1.md` upstream). That is
a separate path and does not take over an existing operator-managed source.

## Editing and validation

`node06-roots.json` opts in only the files under `site-content/`. The localized
entrances connect Games, World, Skills, For developers and Logs. Public skill
cards document the current Arena rules; the source is not a complete game manual
or a publication of internal lore. There are no
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
Owner-managed source registration issues its own proof, followed by
preview and explicit acceptance; do not use it to replace this operator binding. `welcome.mode=git` describes the proposed import; it does
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
graph relations. The five aspects are Games, World, Skills, For developers and Logs. Home translations select different existing
point destinations, without adding language routes or partitioning the graph.

This manifest requires NODE06 main containing `eb3171a` (merged as `29135cf`),
which implements complete home translations. Ensure that engine version is
installed **before** publishing this content; older engines reject the added
fields and retain the last accepted home. No new database migration is needed
for home translations. The existing deployment pipeline publishes data only;
repository files/scripts/HTML are never run by the content publisher.

The main variant is Russian (`default_language=ru`); `translations.en` defines
its own complete introduction, blocks, navigation labels and links. Each Russian block uses its `*-ru` destinations and each English block its
`*-en` destinations. The brand and external game URLs are shared explicitly.
The browser-language/local preference switch and no-JS fallback belong to NODE06.
Existing point IDs are preserved while the public reference adds bodies and
graph relationships through the reviewed content source.

New sites default to automatic priority: accepted Git home, then site settings,
then welcome. Existing saved UI layouts retain their choice on migration. In
`/sites/` the owner can select Auto, Git, site settings or welcome; Git publication
does not erase the saved UI layout or force the owner's selection. Removing the
manifest home clears its accepted Git snapshot at the next successful release;
temporary fetch/validation failure preserves the last accepted snapshot.

## Godot client development log

Four RU/EN stage pairs cover account/session flow, inventory, shared battle
presentation and saved language/settings. Each post links to its index, adjacent
stages and counterpart. The Games and Logs roots link to its index; each home language has a Logs card. Source/history evidence and explicit validation limits:
[Godot devlog evidence](docs/GODOT-DEVLOG-EVIDENCE.md). These posts describe merged
source, not a newly exported or published client. No hidden lore is added.


## Expanded public reference

The starter pack has 16 skill cards per language with source-verified Normal and
Ultimate formulas and links to the eight existing NODE06 triples. Characters,
companies and the campaign have public index points; Andy/Unknown are names and
links only. Developer roots cover static, connected and independent operation;
Logs connects development journals and page-change discussion.

This packet needs the engine's operator-only `md://core/` support before content
publication. Keep the existing site registration and operator deploy binding.
Source/translation/visibility evidence and graph validation:
[Content sources](docs/CONTENT-SOURCES.md).

Validation checkpoint: immutable root preflight accepted 82 points with no graph
warnings. Public source coefficients and all 32 English mode formulas match the
saved catalog. Disposable PostgreSQL publication verified bidirectional skill/
core-triple visibility without copied core revisions. Home acceptance checked
five cards, language-specific destinations and desktop/390px layout. Deployment
remains pending. Install NODE06 core-link support before publishing this source.
