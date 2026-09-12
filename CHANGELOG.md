# Changelog

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
