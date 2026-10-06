# GitHub & Aikido ruleset

## Access

1. Sign in to Aikido with your GitHub account. Before Q1 2027, GitHub sign-in will be routed via Google.
2. Two-factor authentication (2FA) must always be enabled on every account, including your GitHub account (SSO will cover this once it's in place). If 2FA is disabled on any account without IT involvement, we will block access to that account.
3. Only request the access you need. If you no longer need GitHub access, let IT know so they can free up the seat.
4. Always use the available teams to give Loopers access. **Do not** assign permissions to individuals, this is risky and impossible to manage. When in doubt, reach out to IT.
5. Externals (partners, freelancers, etc.) without a loopearplugs.com account can be added as collaborators, only to the specific repos they need and with the least access required. For broader access, such as team-based access, a Loop Earplugs account is always required.

## Roles

6. The default role is **Maintain**. Only assign a different role when the use case requires it, always apply least privilege and avoid assigning the Admin role.

## Findings

7. Repo members are responsible for resolving flagged risks in their repos. This includes repos fully managed by externals: you are responsible for agreeing the required fixes with them and making sure they're resolved within the SLAs.
8. AutoFix is available, but a fix is never applied automatically. Repo members must always assess and deploy it themselves.
9. Flagged risks must be resolved within these SLAs (starting point):
   - Critical: 10 days
   - High: 20 days
   - Medium: 30 days
   - Low: 60 days

## Secure development

10. Changes to the main branch go through a pull request (PR) with at least one reviewer other than the PR author.
11. Never store passwords, keys or tokens in code. If a secret is exposed, rotate it immediately and inform IT.
12. Only use maintained, trusted dependencies and keep them up to date.
13. Product software is never released with known exploitable vulnerabilities.
14. You can't create public repositories. Exceptions are only allowed in select cases, contact IT with your request.
15. Personal repos must not be hosted in the Loop organisation. Host them under your personal GitHub account, and they must not contain Loop intellectual property.

## Incidents

16. Report a suspected security incident or actively exploited vulnerability to IT immediately. NIS2 and the CRA require reporting to authorities within 24 hours, so every hour counts.

## Repo housekeeping

17. Keep your repos clear and concise: use tags and descriptions where possible, and add a README for your fellow devs. You can easily create a README with any of the AI tools available at Loop, including Claude.
18. Repos that are no longer relevant must be archived.
19. Every repo has the custom property `HISTORICAL-ARCHIVE`, set to `false` by default. Archived repos set to `false` will be deleted to keep our GitHub environment clean and audit-ready.
20. If an archived repo must be kept for historical reference, set `HISTORICAL-ARCHIVE` to `true` before archiving it.
21. We use a few other custom properties, such as `GCP-IAC`, to sort and filter repos.

## How to set the custom property

- Open the repo on GitHub, go to **Settings**, click **Custom properties** in the left sidebar, set `HISTORICAL-ARCHIVE` to `true` and click **Save**.
- You need admin access on the repo. If you don't have it, reach out to IT.

## References for GitHub best practices

- [Structuring GitHub Enterprise: Best practices from the org level down](https://dev.to/playfulprogramming/structuring-github-enterprise-best-practices-from-the-org-level-down-45i5)
