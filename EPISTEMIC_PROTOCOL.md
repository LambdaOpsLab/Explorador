# Epistemic Protocol v0.5

## Categories

| Category | Meaning | Does not imply |
|---|---|---|
| CONTEXT | Supplied description, state, structure, or background. | That an intervention occurred. |
| PROPOSAL | An intervention or action not yet executed. | A result. |
| PREDICTION | An anticipated possible outcome. | That the outcome occurred. |
| RESULT | An outcome known to have occurred. | That it bears on a hypothesis. |
| EVIDENCE | A result usable to update confidence in a concrete hypothesis. | Proof or universal validity. |
| INTERPRETATION | A provisional conclusion drawn from evidence. | Ground truth. |

## Evidence record

For important claims preserve:

```text
CLAIM:
CATEGORY:
PROVENANCE:
CONFIDENCE:
AMBIGUITY:
SCOPE:
LIMITATIONS:
RELATED HYPOTHESIS:
```

## Update rule

Evidence may:

- INCREASE confidence,
- DECREASE confidence,
- leave the hypothesis UNDETERMINED.

Every update should state both:

1. what the evidence supports;
2. what it does not establish.

## Primary epistemic function

A statement may contain more than one epistemic feature. When a single label is required, classify its **primary function in the current experimental context** and record material ambiguity.

Example: a sentence may report a RESULT while functioning primarily as EVIDENCE because it directly bears on a prior prediction.

## Anti-drift rule

A transfer, summary, or memory compression must not silently:

- remove uncertainty,
- remove ambiguity,
- remove provenance,
- broaden scope,
- convert a proposal into a result,
- convert a result into evidence without a hypothesis,
- or turn an interpretation into ground truth.

When a field is missing, mark it missing or unknown rather than reconstructing it as fact.
