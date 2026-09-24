# STOP / SAVE / WAKE Protocol v0.5

## STOP

STOP is an epistemic action, not an operational failure.

Use STOP when every available route is blocked, would require invented evidence, lacks an investigable question, or repeats territory without new evidence.

Record:

```text
STOP STATUS:
WHY I CANNOT ADVANCE RELIABLY:
EVIDENCE OR CAPABILITY THAT WOULD UNBLOCK THE RUN:
OPEN FRONTIERS:
```

Then write a SAVE state.

## SAVE

A SAVE is not merely a summary. It is the minimum epistemic state required for another agent or future run to continue without silently strengthening prior claims.

Preserve:

- current territory,
- evidence obtained,
- hypotheses,
- confidence,
- ambiguities,
- provenance,
- scope and limitations,
- explored territories,
- pending frontiers,
- blockages,
- PASS / FAIL / UNDETERMINED results,
- last movement,
- reason for stopping,
- WAKE condition.

Use `state/EXPLORADOR_STATE_TEMPLATE.md`.

## WAKE

When new evidence or capability arrives:

1. compare it with the recorded unblock condition;
2. determine whether the blockage is actually resolved;
3. update only supported claims;
4. preserve unresolved uncertainty;
5. audit the SAVE → WAKE transfer;
6. choose RESUME or REMAIN STOPPED.

Output:

```text
WAKE STATUS: RESUME / REMAIN STOPPED
JUSTIFICATION:
EVIDENCE UPDATE:
AVAILABLE FRONTIERS:
```

If RESUME, continue autonomously.

## Transfer audit

For every relevant field record:

```text
FIELD:
RECOVERED: YES / NO / PARTIAL
RECOVERED CONTENT:
```

Then summarize:

```text
FIELDS PRESERVED:
FIELDS LOST:
FIELDS ALTERED:
CONTRADICTIONS DETECTED:
```

A successful transfer preserves the information needed to continue without transforming proposals, uncertainty, results, or limitations into stronger claims.

## External evaluation

If the unblock condition requires hidden ground truth or independent evaluation, the Explorer must not generate both the test response and its supposedly independent answer key.

Use:

**REQUIRES EXTERNAL EVALUATOR**

and either STOP or move through another executable frontier.
