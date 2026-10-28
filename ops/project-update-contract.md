# Project Update Contract

For conversations inside the user's writing project, treat reusable feedback as a repository-maintenance trigger.

## Required behavior

After completing the user's immediate request, silently ask:

> Did this turn reveal a new durable preference, recipient rule, scenario rule, routing rule, or repeatable failure mode?

If **no**, do not modify the repository.

If **yes**:
1. update the smallest relevant knowledge/agent/routing file;
2. add or update a regression case when appropriate;
3. add a concise CHANGELOG entry;
4. avoid asking the user to manage the agent manually.

## Examples that usually trigger an update

- user repeatedly rejects a tone pattern;
- user says "以後..." or otherwise makes a durable instruction;
- a new recurring administrative task appears;
- a message fails because a rule, deadline, hierarchy, or requested action was unclear;
- the user establishes a consistent recipient-specific preference.

## Examples that usually do not trigger an update

- typo correction;
- one person's one-time name/title change;
- one-off date/amount;
- preference that is explicitly limited to a single message;
- factual correction with no reusable writing lesson.
