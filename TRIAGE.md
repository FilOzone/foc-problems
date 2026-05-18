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

1. Create a sanitized downstream issue in the destination repo.
2. Include only public-safe details.
3. Link the downstream issue from the intake issue.
4. Link the intake issue from the downstream issue when appropriate.
5. Add `routed` to the intake issue.
6. Close the intake issue when the downstream issue is the active tracking location.

If a matching issue already exists, link it, add `duplicate`, and close the intake issue with a short note.

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
