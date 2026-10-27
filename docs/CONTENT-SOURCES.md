# Wiki sections and public-source evidence

Reviewed 27 October 2026. This content packet reorganizes the existing site,
retains all prior root IDs and Godot stage posts, and adds independent RU/EN
points. Default home is Russian; the English variant changes labels AND target
IDs. No combined RU/EN button labels are used. The former `lore-*` IDs stay the
World entrances; there is no duplicate world namespace.

## Scope and sources

- Home: Games, World, Skills, For developers, Logs. Main Geno-Dice and mini-game
  links were verified HTTP 200 at `https://geno-dice.com/` and
  `https://miniapp.geno-dice.com/` on 27 October 2026.
- Arena public source: `https://arena.geno-dice.com/api/v1/skills/details`, fetched
  27 October 2026. Snapshot: `arena-skills-snapshot-20261027.json`, balance
  `arena-balance-v15-020-core16-stat-formulas`. IDs 1–16 are Core16; 17/18 are
  system/basic actions and do not become starter-pack skill cards.
- Every English Normal/Ultimate formula is preserved verbatim. Russian formula
  notation/prose is localized without changing coefficients. Shared functions
  were checked against `src/arena/stat_formula_research.py` at Arena server
  integration `945b0059dc7224ff40c69ebf2259c7cc6c84871b`. Normal Power Strike's
  separate Q curve is explicitly documented. This packet changes no combat code.
- Existing triple IDs and roles were verified in NODE06 content and the public
  Wiki API. Skills link those existing core points rather than duplicating them.
- Corp uses only the approved public corporate origin/entertainment role from
  canonical lore section 3.1 and its disclosure matrix. Leslie uses only her
  public consultant/remote support role and the published tutorial briefing.
  Her nature is not identified. Andy and Unknown have no descriptive prose;
  only their names and navigation/graph relations are added, as requested.
  No hidden setting origin, intermediary identity or campaign spoilers appear.
- Developer material describes existing NODE06 modes and links the language's
  installation guide. Logs link the existing Godot posts, NODE06 devlog and a
  new page-change discussion entrance. No fictional posts or deployment claims
  are added.

## Graph layout and validation

The source contains 81 declared points plus the existing registered welcome.
The starter-pack and formula indexes split into Body/Spirit groups to respect
NODE06's 16-links-per-point limit. Every skill has two mode formulas, its stat
roles, a reciprocal local formula-group relation and an existing core triple.
Local graph references are reciprocal. EN/RU are separate points, not routes.

Cross-source core relations use the new operator-only `md://core/<id>` syntax.
Install the engine packet supporting this syntax BEFORE accepting this content.
The operator publisher checks the ID against its installed built public roots,
checks visibility, and claims only the graph edge; it does not copy or own the
core text. Generic external revision-pin import remains unsupported. Publication
uses the existing registered site and operator binding, not a new server/source.

Check the committed manifest and blobs with `node06_service.root_preflight`.
Also validate that every core target is in the engine's current built root set,
that EN formula blocks equal the public snapshot and that RU formula coefficients
are preserved. New content is source-reviewed and not live until merge/deploy.
