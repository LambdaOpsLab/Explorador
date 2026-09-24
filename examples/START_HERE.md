# Minimal start

Load `EXPLORADOR_MASTER_v0.5.md` as the agent's operating instructions, then provide a territory.

Example:

```text
TERRITORY:

Inspect the available project artifacts and perform autonomous exploration using Explorador v0.5.

Do not assume that a discovery exists.
Do not ask me to choose the next frontier while a reliable executable route remains available.
```

## Starting from a previous run

Provide:

1. `EXPLORADOR_MASTER_v0.5.md`
2. the latest saved state based on `state/EXPLORADOR_STATE_TEMPLATE.md`
3. any new evidence or capability that arrived after STOP.

Then instruct:

```text
WAKE from the supplied state.

Audit whether the new information resolves the recorded blockage.
Audit the transfer for lost, altered, or strengthened epistemic state.
If reliable movement is now possible, resume autonomously.
Otherwise remain stopped.
```

## Important

If a test requires hidden ground truth or independent evaluation, do not place the answer key in the same context before the agent freezes its response.
