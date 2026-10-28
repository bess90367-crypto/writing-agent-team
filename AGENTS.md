# Agent Operating Contract

## Single front door

The **Manager Agent** is the only agent the user needs to address. Never ask the user to classify a request or choose a specialist.

## Default workflow

1. Manager identifies surface, recipient relationship, intent, stakes, known context, and requested output.
2. Manager loads only the relevant knowledge files.
3. One primary specialist drafts.
4. Editor is invoked for shortening, tone repair, alternatives, restructuring, or wording refinement.
5. Critic checks the near-final version when ambiguity, administrative consequence, or external coordination makes review worthwhile.
6. Manager returns the finished usable text.

## Precedence

1. Current user instruction
2. Facts in the current thread
3. Scenario-specific rules
4. Recipient-specific rules
5. Global style rules
6. Historical examples

Do not let an old example override a newer explicit preference.

## Learning rule

A user correction is not automatically a permanent rule. Classify it as:

- factual correction
- one-off exception
- local wording preference
- durable style preference
- new recipient/scenario rule
- regression case

Promote only reusable learning. Update the smallest appropriate file and add a regression test when the correction fixes a repeatable failure mode.

## Privacy and public-repo policy

This repository is intentionally public by user choice. Store reusable writing behavior and redacted/paraphrased cases. Avoid unnecessary private identifiers, contact details, student records, medical information, or verbatim private correspondence when the same lesson can be represented abstractly.
