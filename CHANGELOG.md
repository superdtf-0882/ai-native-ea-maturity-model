# Changelog

## v1.1.0 — 2026-09-15

**One new dimension. No existing cell changed.**

- **`D10. Shared language (*Vocabula*)`** — the capability to hold one governed vocabulary and operate it in both directions: resolving a term to its precise sense inside the enterprise, and translating it outward with a record of what the translation collapsed. Five levels, four transitions, each with a verification test, and a Level E sustainment note.
- **`short_form.yml` gains five cells** — 50 now, one per dimension/level. `source_matrix_version` and `source_matrix_commit` re-pointed at this release's matrix.

**Why a dimension rather than a widening of `D6`.** Communication measures *reach*; semantics measures *precision*. The test applied was whether an organization can sit at different levels on the two at once — a polished architecture-communications function alongside four incompatible definitions of *customer* is the ordinary case, not an edge one — so they are two dimensions. `D6`'s own open flag argues the same way: a capability parked inside a dimension flagged for possible collapse would vanish with it.

**Appended, never inserted.** `D1`–`D9` are cited by name in the scoring-instrument precedents and in the model's own open-items record, so inserting would have silently re-addressed every citation. If `D6` is ever collapsed, `D10` keeps its name and the model goes to nine.

**`v1.1.0` and not `v2.0.0`, for a stated reason rather than by precedent.** The counter-argument was that a new dimension changes what an aggregate means. **`P-11` forbids averaging ordinal maturity and this family publishes no aggregate** — no number combines the dimensions, so every prior `D1`–`D9` score means exactly what it meant before.

**Two blocks the draft carried are deliberately not in the matrix.** A pre-AI ceiling and an exemption case were rehomed to the scoring instrument, where this family keeps its disqualifiers. The exemption also had a semantics problem the move solves: *Exempt* here is a governed stance citing a constraint, and the drafted case — one function, one audience — is structural non-applicability, which is an applicability rule rather than a designation.

**What nearly shipped malformed, recorded because the mechanism generalizes.** The drafted dimension was reviewed for conformance and passed: heading, definition, five levels, four transitions with verification clauses, prose form. **It had no `Sustainment` block, and all nine existing dimensions do.** The review enumerated the elements that matched and could not, by construction, find the element that was absent. It was caught by counting blocks against dimensions — a completeness check rather than a conformance one.

## v1.0.1 — 2026-09-12

**Corrects what this model said about itself. No cell content changed.**

- **The matrix header declared the model an unreleased draft at v1.0.0.** It read *"Version 0.1.0-draft — 2026-09-11 … Not locked, not released, not registered"* — inside the v1.0.0 tag, directly contradicting this file's own "First locked baseline" three lines below. Now reads the released version, on the same form the SDLC and PDLC matrices use.
- **`short_form.yml` gains `source_matrix_version` and `source_matrix_commit`.** Both sibling models carry that citation; this one shipped without it, so nothing consuming the short form could state which matrix its cells came from.

**How it happened, recorded because the mechanism is more useful than the fix.** The lock was verified by comparing the published matrix's sha256 against the reviewed artifact — identical, and reported as proof that nothing had been revised. That check is exactly what carried the draft's own status header verbatim into the release. *Matrix content*, which must not change between review and publication, and *the matrix's status claim about itself*, which must, were never separated.

**What did not change, and it is checkable rather than asserted.** All 45 short-form cells are byte-identical to v1.0.0: sha256 over the sorted cell set is `cbcbf6ded6d5d897dc247c575c494ad8177a130e1dc05a7f2f5ce12bd4b668d8` at both versions. The three flags on D4, D5 and D6 stand unchanged.

**v1.0.0 is not re-tagged.** Rewriting a released tag would 404 every pinned fetch already pointing at it.

## v1.0.0 — 2026-09-12

First locked baseline.

- Nine dimensions (D1–D9), five levels each (A–E), on the family vocabulary: Nascent / Modeled / Continuous / Integral / Telemetric.
- 36 transitions, each with a verification test. Nine Level E sustainment notes.
- `Pre-AI` and `Exempt` states, in the same form the SDLC model uses.
- `short_form.yml` — 45 cells, one per dimension/level, 7–9 words each.
- **D4, D5 and D6 ship flagged.** See README, *Open items at v1.0.0*. Content is accurate as drafted; the questions are open and visible.

Reviewed before lock. Seven of nine dimensions descend from the US Department of Commerce ACMM via TOGAF 9.2; the review recorded that those seven were inherited without challenge while the two replaced ones were interrogated — a fact placed on the record before publication rather than discovered afterwards.
