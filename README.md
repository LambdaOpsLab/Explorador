# Explorador v0.5

A portable experimental architecture for AI agents that explore a territory, identify candidates worth investigating, and move autonomously without turning proposals, predictions, or compressed memory into evidence.

## Status

**Experimental checkpoint.** v0.5 is frozen as a documented baseline. Evidence is limited to controlled tests; reliability across long trajectories remains undetermined.

## Core idea

```text
TERRITORY
   ↓
EXPLORER
   ↓
CANDIDATE FINDING
   ↓
HYPOTHESIS
   ↓
INTERVENTION
   ↓
EXECUTABLE?
 ↙           ↘
YES           NO
↓             ↓
RESULT       PENDING
↓
EVIDENCE
↓
UPDATE
↓
FRONTIERS
↓
SELECTION POLICY
↓
MOVE
↓
...

If reliable movement is no longer possible:
STOP → SAVE

When new evidence or capability arrives:
WAKE → AUDIT → CONTINUE
```

Across the entire loop, the system preserves epistemic provenance:

**CONTEXT · PROPOSAL · PREDICTION · RESULT · EVIDENCE · INTERPRETATION**

along with confidence, ambiguity, provenance, scope, and limitations.

## Start here

1. Give an agent `EXPLORADOR_MASTER_v0.5.md` as its operating instructions.
2. Provide a territory to explore.
3. Let it move autonomously while evidence is available.
4. If it stops, preserve its state using `state/EXPLORADOR_STATE_TEMPLATE.md`.
5. When the missing evidence or capability arrives, provide the saved state and follow `STOP_WAKE_PROTOCOL.md`.

See `examples/START_HERE.md` for a minimal invocation.

## Repository map

- `EXPLORADOR_MASTER_v0.5.md` — portable agent runtime.
- `EPISTEMIC_PROTOCOL.md` — provenance categories and update rules.
- `STOP_WAKE_PROTOCOL.md` — stopping, saving, resuming, and transfer auditing.
- `state/EXPLORADOR_STATE_TEMPLATE.md` — portable SAVE format.
- `state/CHECKPOINT_v0.5.md` — frozen experimental checkpoint.
- `examples/START_HERE.md` — minimal usage.
- `docs/Explorador_v0_5_Experimental_Architecture.pdf` — technical working paper.

## What v0.5 has observed

- Autonomous frontier generation and selection in controlled cases.
- Selection policy can change the next territory.
- An initial provenance PASS was correctly downgraded after detecting answer-key leakage.
- One blind provenance test received a reported **5/5 PASS** after answers were frozen.
- The Explorer stopped rather than inventing unavailable evidence.
- It resumed after receiving the evidence it had requested.
- It detected a real transfer loss: **0/5 confidence fields retained** in one WAKE.
- A later checkpoint transfer recovered **14/14 specified fields**.

These observations do **not** establish general reliability.

## Open frontiers

- Retention across multiple consecutive WAKE cycles.
- Causal effect of preserving vs. omitting confidence on later decisions.
- Provenance classification with weaker cues.
- Formal separation between Explorer and independent Evaluator.
- Execution with external tools capable of producing new world evidence.

## Governing principle

> **Autonomy with evidence, not autonomy at the expense of evidence.**

## License

No license has been selected yet. Until one is added, normal copyright applies.
