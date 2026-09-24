# CHECKPOINT — EXPLORADOR v0.5

Status: **frozen experimental checkpoint**

## Observed capabilities

- Classified five new cases with frozen answers; a later external evaluation reported 5/5 agreement with ground truth.
- Preserved an explicit ambiguity in one case and recorded MEDIUM confidence for it.
- Detected that an earlier provenance test exposed its own answer key and narrowed what that PASS could establish.
- Detected the loss of all five confidence fields in a WAKE transfer.
- Stopped when continuing would have required treating proposals or repetition as new evidence.
- Resumed after receiving the new evidence it had explicitly requested.
- Audited a later checkpoint transfer and recovered 14/14 specified fields.

## Experimental results

### PASS — reported blind test

One blind test, five cases, reported 5/5 after answers were frozen.

**Scope:** one execution.

**Does not establish:** general provenance-classification reliability.

### Observed transfer loss

The first WAKE preserved:

- 5/5 classifications,
- 1/1 recorded ambiguity,
- 0/5 confidence levels.

This established an information loss in that transfer.

It did **not** establish that the loss changed a later decision.

### PASS — compact record

A structured record successfully recovered the fields that had been inserted into it.

This did **not** establish that future agents would populate those fields correctly or preserve them over long chains.

### PASS — final checkpoint transfer

14/14 specified fields were recoverable from the supplied checkpoint.

This did **not** establish indefinite retention over multiple WAKE cycles.

## Undetermined

- Generalization of provenance classification.
- Retention across multiple consecutive WAKE cycles.
- Effect of omitting confidence on later decisions.
- Performance with weaker provenance cues.

## Emergent architecture

The experimental trajectory identified the need for:

- an exploration loop,
- explicit epistemic provenance,
- frontier selection policy,
- executable vs. non-executable intervention gating,
- STOP,
- SAVE,
- WAKE,
- an epistemic state record,
- transfer auditing,
- and separation between Explorer and independent Evaluator when ground truth must be hidden.

These components are partially tested protocol elements, not a fully demonstrated autonomous research system.

## Open frontiers

1. Retention across multiple WAKE cycles.
2. Causal effect of preserving or omitting confidence on later decisions.
3. Provenance classification with less explicit material.
4. Formal Explorer/Evaluator separation.
5. Tool-enabled acquisition of new external evidence.

## Conclusion

Explorador v0.5 has shown, in controlled cases, the ability to explore, open frontiers, choose, stop when evidence is unavailable, resume when evidence arrives, and audit continuity of state.

It also recorded real failures rather than hiding them.

Reliability across long trajectories remains **UNDETERMINED**.
