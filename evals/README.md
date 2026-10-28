# Evaluation Strategy

The goal is not to score literary quality. It is to catch repeatable failures that matter in the user's real workflow.

## Regression dimensions

1. **Clarity** — purpose and requested action are identifiable.
2. **Completeness** — necessary date/deadline/process/consequence is retained.
3. **Brevity** — no unnecessary retelling.
4. **Tone** — respectful, natural, not bureaucratic or coercive.
5. **Fidelity** — no invented facts or commitments.
6. **Recipient fit** — student/faculty/external/vendor styles differ appropriately.
7. **Surface fit** — LINE is not written like email; email is not written like official-document prose.
8. **Variant quality** — requested alternatives are meaningfully different.

## How to use

When a durable rule changes:
- run the relevant cases conceptually or with an LLM harness;
- add a new case for the failure that triggered the change;
- do not delete an old case unless the underlying preference was explicitly reversed.
