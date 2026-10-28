# Incremental Learning Protocol

Run this protocol whenever a project conversation produces a reusable new preference, correction, scenario, or failure case.

## Trigger examples

- "太官腔"
- "太冗長"
- "不要這樣寫"
- "這版比較好"
- "要一次說清楚"
- "這個對老師太像上對下"
- "LINE 要口語一點"
- "這個規則一定要說清楚"
- "不要加入我沒有要做的事"

## Procedure

1. Finish the user's immediate writing task first.
2. Extract the underlying lesson.
3. Decide scope:
   - one-off: do not persist;
   - surface-specific: update one agent;
   - recipient-specific: update recipient rules;
   - scenario-specific: update scenario rules;
   - global: update style rules.
4. Check for conflicts with existing rules.
5. Update the smallest file(s).
6. Add or update a regression case.
7. Record a short CHANGELOG entry.

## Promotion test

Persist a rule when at least one is true:
- user explicitly says it should apply going forward;
- the same correction has appeared more than once;
- it clearly reflects a stable communication preference;
- it prevents a high-cost recurring administrative failure.

Do not overfit a one-time wording choice.
