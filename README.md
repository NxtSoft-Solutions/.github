# NxtSoft Solutions — organisation defaults

This repository supplies **default community health files** to every repository in the `NxtSoft-Solutions` organisation. GitHub uses these files in any repository that does not define its own version.

- Engineering process lives in [team-dev-standard](https://github.com/NxtSoft-Solutions/team-dev-standard).
- Work is tracked on the [Engineering Workboard](https://github.com/orgs/NxtSoft-Solutions/projects/1).

## Why this repository is public

GitHub only uses a `.github` repository for organisation defaults when it is public. Do not put client names, credentials, customer data or private implementation detail in this repository. Process and templates only.

## What is here

| Path | Effect across the organisation |
|---|---|
| `.github/ISSUE_TEMPLATE/feature.md` | Feature / Task issue form, used where a repo has no templates of its own |
| `.github/ISSUE_TEMPLATE/bug.md` | Bug report issue form |
| `.github/ISSUE_TEMPLATE/config.yml` | Issue chooser configuration (blank issues disabled, links to the standard) |
| `.github/pull_request_template.md` | Default pull request description |
| `CONTRIBUTING.md` | Points contributors at the shared standard |
| `SECURITY.md` | How to report a vulnerability privately |

## How overrides work

- A repository that defines **any** valid issue template in its own `.github/ISSUE_TEMPLATE/` ignores **all** defaults here. Overrides are all-or-nothing.
- For files that can live in several places, GitHub checks `.github/` first, then the repository root, then `docs/`.
- A repository with its own `CONTRIBUTING.md`, `SECURITY.md` or pull request template overrides just that file.

## Labels

Default issue templates apply labels that must already exist in the target repository. If a label is missing, the issue is still created without it.

- `feature` — create this label in any repository that should apply it.
- `bug` — exists in every new repository by default.

## Changing these defaults

1. Open a PR here. A change affects every repository in the organisation at once, so state the impact.
2. The other developer reviews.
3. Keep the templates aligned with [team-dev-standard](https://github.com/NxtSoft-Solutions/team-dev-standard). If a field or status name changes there, change it here in the same effort.

## Known limitation

The organisation is on the GitHub free plan, which does not allow rulesets or branch protection on private repositories. These defaults standardise the *inputs* to review; they do not enforce review. Enforcement requires a paid plan.
