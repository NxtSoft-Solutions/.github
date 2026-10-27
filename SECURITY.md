# Security Policy

## Reporting a vulnerability

**Do not open a public issue, discussion or pull request for a security problem.**

Report it privately using one of these routes:

1. **GitHub private vulnerability reporting** — on the affected repository, open the **Security** tab and use *Report a vulnerability*. Preferred, because it keeps the report, discussion and fix advisory in one place.
2. **Direct contact** — if private reporting is not enabled on the repository, contact the repository maintainers through the team's private channel and name the repository and affected component.

Include what you can: affected repository and version or commit, the impact, reproduction steps, and whether the issue is already public.

## What happens next

- Acknowledgement within one working day.
- Triage and a severity assessment, using the priority definitions in the shared standard.
- A fix, a regression test and a security advisory where the issue is significant.
- Credit if you want it.

## Scope

In scope: authentication and authorization flaws, injection, data exposure, insecure defaults, exposed credentials, dependency vulnerabilities with a realistic exploit path.

Out of scope: findings from automated scanners with no demonstrated impact, missing hardening headers on non-production hosts, and social engineering of team members.

## Handling an exposed secret

If a credential is committed or leaked:

1. Rotate it immediately. Removing the commit is not sufficient.
2. Check provider audit logs for use of the exposed credential.
3. Record the incident on a `security` issue, including impact and remediation.
4. Add a preventive control so it does not recur.

Full checklist: [security checklist](https://github.com/NxtSoft-Solutions/team-dev-standard/blob/main/docs/processes/security-checklist.md).
