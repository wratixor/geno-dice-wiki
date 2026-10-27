# Formulas

Arena formulas: `arena-balance-v15-020-core16-stat-formulas`, checked against the public catalog on 27 October 2026. These are current Arena combat calculations, not universal coefficients for every Geno-Dice game.

Use the cube's aggregate combat stats, not only the rolled face. Normal mode covers tiers I–III; Ultimate covers IV–VI.

`Q(x) = C(x) / C(ref)`, with `ref = 80` for Normal and `125` for Ultimate; Q80 always uses 80. C is smooth without a gameplay clamp: asymptotes 0.289 and 2.933, anchors C(65)=1 and C(140)=29.28/13.18.

Each curve has the form `C(x) = L + (U-L) / (1 + exp(-k × (x-m)))`. For anchors `(x1,y1)` and `(x2,y2)`, set `p_i=(y_i-L)/(U-L)` and `logit(p)=ln(p/(1-p))`; then `k=(logit(p2)-logit(p1))/(x2-x1)` and `m=x1-logit(p1)/k`.

Exception: Normal Power Strike uses a separate Q curve with asymptotes 0.80 and 1.25 and anchors `(65, 13.18×9.10/125.664)` and `(95, 19.50×6.80/125.664)`. Its Ultimate uses the general C.


`bias(A,O) = (A-O)/(A+O+20)`. `E25(A/O) = 1 + 0.25 × bias(A,O)`; E30 uses 0.30. Opposing pairs: Body—Spirit, Onslaught—Self-Control, Reaction—Technique.

Named curves: SmokeCurve is smoke mitigation; DanceCurve is dance self-exhaustion; VampCurve is the vampiric return fraction. They are smooth curves rather than fixed percentages. Skill formulas show dependencies and calibration coefficients; combat rules determine charge/effect resolution order.

Physical damage passes through Guard to Endurance. Psychic damage targets Psyche; a target holding Impulse takes a 0.80 multiplier, and damage does not consume Impulse by default. Guard and Impulse each have a three-charge limit.

[Public Arena formulas and descriptions](https://arena.geno-dice.com/skills) · [Catalog data](https://arena.geno-dice.com/api/v1/skills/details)

[Formulas for Body triples](md://local/formulas-body-en) · [In Russian](md://local/formulas-ru) · [Formulas for Spirit triples](md://local/formulas-spirit-en) · [Skills](md://local/skills-en) · [Geno-Dice starter pack](md://local/starterpack-en)
