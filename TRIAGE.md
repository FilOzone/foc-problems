# FOC Problem Triage

This runbook is for FOC maintainers triaging reports in `FilOzone/foc-problems`.

## Goals

- Keep user-reported problems from getting lost in Slack.
- Gather enough information to reproduce or route the issue.
- Avoid exposing sensitive details in public downstream issues.
- Route work to the right repo while keeping the intake issue linked.

## First Response

For each new issue:

1. Confirm whether it is a user problem, question, duplicate, or security-sensitive report.
2. Apply labels that describe the current state.
3. Ask for missing information if the issue cannot be triaged.
4. If it came from Slack, link the relevant thread.
5. Decide whether to handle it here or route it to a destination repo.

## Routing

When routing to another repo:

1. Do not transfer the intake issue out of `FilOzone/foc-problems`.
2. Create a sanitized downstream issue in the destination repo.
3. Include only public-safe details.
4. Add a formal GitHub issue relationship between the intake issue and the downstream issue.
5. Link the downstream issue from the intake issue as a human-readable backup.
6. Link the intake issue from the downstream issue when appropriate.
7. Add `routed` to the intake issue.
8. Close the intake issue when the downstream issue is the active tracking location.

The `foc-problems` issue should remain the intake record. The destination repo issue is the active engineering or documentation tracking issue.

## Duplicates

If a matching issue already exists:

1. Add `duplicate` to the intake issue.
2. Use GitHub's "Close as duplicate" functionality so the duplicate relationship is recorded.
3. Add a short comment if extra context would help future triagers.

If GitHub's duplicate close action is not available in the current UI, link the canonical issue in a comment and close the intake issue as a duplicate.

## Security-Sensitive Reports

Do not triage security vulnerabilities in this public repo.

If a report appears security-sensitive:

1. Remove or redact sensitive details if necessary and possible.
2. Point the reporter to the FilOzone security process:
   https://github.com/FilOzone/.github/blob/main/SECURITY.md
3. Add `security-do-not-use`.
4. Close the issue once the reporter has been redirected.

## Suggested Labels

- `needs-triage`: new report waiting for initial review
- `needs-info`: blocked on more information from the reporter
- `blocker`: blocking production or mainnet use
- `routed`: routed to a destination repository or active tracking issue
- `duplicate`: duplicate of another issue
- `not-reproducible`: not reproducible with available information
- `out-of-scope`: not actionable for the FOC team
- `security-do-not-use`: security-sensitive report that should not be handled here

## Triage Cadence

During the MVP pilot, review new reports at least once per business day. If intake volume grows, add automation for project-board routing and stale `needs-info` follow-ups.
