# AI-Native EA Maturity Model

A maturity model appraising an organization's enterprise architecture capability in an AI-native operating model — not the elegance of a single artifact or framework adoption. It is one of the AI-native maturity models, sharing the family's five-level ladder — Nascent / Modeled / Continuous / Integral / Telemetric. For the family, see aimaturitymodels.com/models.

**Versions.** The release tag versions the repository, and the model's version line names the tag it is at, every release (STD-MODEL-PARTS v1.1 §4C). `CHANGELOG.md` says what each release changed.

## What this is

Ten dimensions, each scored on the family-wide five-level ladder. See `ai_native_ea_maturity_model.md` for the full matrix — the source of truth. `short_form.yml` is a compression of it, not a replacement.

## Lineage, stated plainly

Seven of the ten dimensions descend from the US Department of Commerce ACMM, carried through The Open Group's TOGAF 9.2 *Architecture Maturity Models* chapter. **Two were replaced:** IT Investment & Acquisition Strategy became **D8 Strategic Portfolio Management**, and IT Security became **D7 Governance & Authority Plane**. **D10 Shared language is this model's own**, added at v1.1.0.

## Scope boundaries

- **No inheritance from a shared market-intelligence layer.** Enterprise architecture is not a market-facing function.
- **The security programme is out of scope.** Data protection, secrets hygiene, vendor risk and regulatory security compliance are excluded. What D7 carries instead is **reachability** — whether an authority boundary has been established against the surface it actually covers. This is stated as a boundary rather than left as an absence, because IT Security's slot was vacated and silence would read as oversight.

## Open items at v1.0.0

Three dimensions ship with **visible flags**. A flag is not a maturity judgment: the cell content is accurate as drafted, and the underlying question is open. They are rendered rather than dropped. **The flags themselves live in the matrix, under `### Flags`** — the words below describe the same three questions in this README's own voice, and the matrix is where they are stated.

- **D4 — the name.** ACMM's *Senior management involvement* measures whether executives care. These levels measure whether executives author foundational intent and trust the substrate to bind execution. *Intent Authorship* may name it better.
- **D5 — the premise.** *Participation* is a 1999 word for units consuming a central architecture. Level D has units deploying their own agents that inherit central constraints, which is federation rather than participation.
- **D6 — separateness.** If the substrate is queryable and speaks, communication may be a property of D2 rather than a capability beside it. Collapsing it would take the model to nine dimensions.

All three were raised against the drafting pass by the role that performed it, before publication rather than after.

## Not in this repository

The **scoring instrument** — disqualifiers and appraisal procedure — is a separate artifact. The **deep dives** are forthcoming.

## Licence

CC BY 4.0. See `LICENSE.md`.
