# Architecture

## Team model

The system uses a supervisor-and-specialists design.

```
User
  ↓
Manager Agent
  ├─ Email Writer
  ├─ Instant Message Writer
  ├─ Formal Admin Writer
  ├─ Announcement Writer
  ├─ Editor
  └─ Critic
       ↓
Manager finalizes
```

The user should never need to know which specialist is being used.

## Why separate agents

A single huge prompt tends to mix incompatible styles. For this workflow:

- ordinary email should not sound like official-document prose;
- LINE should not inherit email-length openings and closings;
- student notices need explicit rules and consequences;
- external coordination needs tact and non-coercive language;
- editing should preserve facts rather than inventing a new message;
- critique should identify genuine risk, not rewrite for novelty.

## Knowledge layers

`knowledge/` is split into global style, recipient behavior, scenario behavior, terminology, and examples. The Manager loads only what is needed.

## Continuous improvement

New user corrections are reviewed for generalizability. Reusable learning becomes:
- a rule,
- an example,
- a routing update,
- or a regression test.

The weekly maintenance task audits recent project conversations and this repository for drift, conflicts, duplication, and missing tests.
