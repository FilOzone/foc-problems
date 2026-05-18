# FOC Problems

Public intake repo for Filecoin Onchain Cloud (FOC) user problem reports.

Use this repo when a discussion in `#fil-foc` or another support channel turns into something the FOC team should track, triage, deduplicate, and route to the right project or repository.

## Report a Problem

Open a new report here:

https://github.com/FilOzone/foc-problems/issues/new/choose

The issue form asks for the information that usually helps triage:

- affected product or component
- urgency and impact
- version or environment details
- expected vs. actual behavior
- reproduction steps
- public identifiers such as pieceCID, provider IDs, job IDs, deal IDs, or transaction CIDs
- redacted logs or screenshots
- Slack thread link, if the problem started in `#fil-foc`

## Public Visibility

This repository is public. Anyone can read the issues filed here.

Do not include:

- secrets, access tokens, credentials, private keys, or seed phrases
- sensitive customer data
- unredacted logs
- private contact details unless you are comfortable sharing them publicly
- security vulnerability details

If the issue may be security-sensitive, follow the FilOzone security reporting process instead:

https://github.com/FilOzone/.github/blob/main/SECURITY.md

## What Happens Next

FOC triagers will review new reports, ask for missing information, deduplicate related reports, and route the problem to the right repository or team.

Depending on the issue, the triage outcome may be:

- the issue is handled directly here
- a sanitized issue is created in a destination repository
- the report is linked to an existing issue
- more information is requested
- the issue is closed as duplicate, not reproducible, or out of scope

See [TRIAGE.md](TRIAGE.md) for the triage workflow.
