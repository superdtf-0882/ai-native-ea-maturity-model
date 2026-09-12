# AI-Native EA Maturity Model

A maturity model appraising an organization's enterprise architecture capability in an AI-native operating model — not the elegance of a single artifact or framework adoption. Part of the same family as the [AI-Native SDLC Maturity Model](https://github.com/superdtf-0882/ai-native-sdlc-maturity-model), the [AI-Native PDLC Maturity Model](https://github.com/superdtf-0882/ai-native-pdlc-maturity-model) and the [AI-Native Product Prioritization Maturity Model](https://github.com/superdtf-0882/ai-native-product-prioritization-maturity-model), sharing the same five-level vocabulary — Nascent / Modeled / Continuous / Integral / Telemetric.

## What this is

Nine dimensions, each scored on the family-wide five-level ladder. See `ai_native_ea_maturity_model.md` for the full matrix — the source of truth. `short_form.yml` is a compression of it, not a replacement.

## Lineage, stated plainly

Seven of the nine dimensions descend from the US Department of Commerce ACMM, carried through The Open Group's TOGAF 9.2 *Architecture Maturity Models* chapter. **Two were replaced:** IT Investment & Acquisition Strategy became **D8 Strategic Portfolio Management**, and IT Security became **D7 Governance & Authority Plane**.

## Scope boundaries

- **No inheritance from a shared market-intelligence layer.** That layer is market-scoped; enterprise architecture is not a market-facing function.
- **The security programme is out of scope.** Data protection, secrets hygiene, vendor risk and regulatory security compliance are excluded. What D7 carries instead is **reachability** — whether an authority boundary has been established against the surface it actually covers. This is stated as a boundary rather than left as an absence, because IT Security's slot was vacated and silence would read as oversight.

## Open items at v1.0.0

Three dimensions ship with **visible flags**. A flag is not a maturity judgment: the cell content is accurate as drafted, and the underlying question is open. They are rendered rather than dropped.

- **D4 — the name.** ACMM's *Senior management involvement* measures whether executives care. These levels measure whether executives author foundational intent and trust the substrate to bind execution. *Intent Authorship* may name it better.
- **D5 — the premise.** *Participation* is a 1999 word for units consuming a central architecture. Level D has units deploying their own agents that inherit central constraints, which is federation rather than participation.
- **D6 — separateness.** If the substrate is queryable and speaks, communication may be a property of D2 rather than a capability beside it. Collapsing it would take the model to eight dimensions.

All three were raised against the drafting pass by the role that performed it, before publication rather than after.

## Not in this repository

The **scoring instrument** — disqualifiers and appraisal procedure — is a separate artifact, as it is for the sibling models. The **deep dives** are forthcoming.

## Licence

CC BY 4.0. See `LICENSE.md`.
