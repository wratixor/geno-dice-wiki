# Content authoring

This repository contains public content only, not application code.
The configured origin identifies the repository; NODE06 owns the import contract.

- Keep the existing registered site ID in `node06-roots.json`.
- Russian and English are independent points in one graph, never locale routes.
- Use reciprocal `md://local/<id>` links for graph relationships.
- Put only explicitly public, source-verified material here. Do not copy hidden
  lore, internal design notes, credentials or database exports.
- Do not invent mechanics, canonical details or claim import is deployed.
- Validate the committed manifest and blobs with NODE06 root preflight.
- Use reviewed feature branches targeting main. Do not add application workflows
  or deploy hooks to this content source.
