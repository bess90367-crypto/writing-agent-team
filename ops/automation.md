# Automated Maintenance

## Hourly self-optimization

An active scheduled task reviews recent 「寫信」 project conversations against the writing-agent repository.

Current cadence:
- every 1 hour (the accepted alternative to the requested 30-minute interval)
- timezone: Asia/Taipei

On each run:
1. look for durable preferences, corrections, new recurring scenarios, and failure modes;
2. check for contradictory, duplicate, over-broad, or stale rules and missing regression cases;
3. make the smallest necessary GitHub update, including CHANGELOG when behavior changes;
4. make **no repository change** when there is no substantive improvement.

## Weekly deeper review

A separate active scheduled task performs a more comprehensive audit.

Current cadence:
- weekly, Monday morning
- timezone: Asia/Taipei

The deeper review follows `ops/weekly-review.md`.

## Purpose and boundaries

The schedules are safety nets, not substitutes for incremental updates. Reusable feedback should still be incorporated when it appears.

A scheduled review is **recurring maintenance**, not a one-time goal that ends after a successful run. Do not create a new task each run, and do not stop the existing recurring tasks merely because one review found no changes.
