<div align="center">

# Tony Thomas

**Senior Manager, Software Development & Standards at Integrated Services of Kalamazoo. I lead the team that designs, builds, deploys, and hosts ISK's own software.**

[![ISK](https://img.shields.io/badge/Integrated%20Services%20of%20Kalamazoo-2E55A5)](https://www.iskzoo.org) [![LinkedIn](https://img.shields.io/badge/LinkedIn-2E55A5)](https://www.linkedin.com/in/thomas9164/) [![Email](https://img.shields.io/badge/email-AThomas%40iskzoo.org-5AB65F)](mailto:AThomas@iskzoo.org)

</div>

---

## Improving Outcomes

Two sessions in the IT track at the CMHA Improving Outcomes Winter 2026 conference in Ypsilanti.

| Session | What it covers | Resources |
|---|---|---|
| **Build, Deploy, Host: Internal Software Development at a CMHSP**<br>Thursday, November 5, 2026 · 2:00 PM | How a mid-sized agency designs, builds, deploys, and hosts its own enterprise software: the stack, the source control and code review standards, automated testing, environment separation, and the pipeline that moves a change into production. Lantern, the app that replaced our annual provider audit, is the running example. | Slides, posted here after the session |
| **AI In Action: Prompting, Productivity and Real-World Organizational Use Cases**<br>Thursday, November 5, 2026 · 3:15 PM, with Warwick Barlow | Five Claude Code agents, each defined in one Markdown file, build a policy library web app during the session. A coordinator writes the contract, a backend developer and a frontend developer build to it at the same time, a verifier proves it works, and a reviewer checks the code. | [Companion repo](https://github.com/tthomas-ISK/IO-Conference__Agents): the agent files, hooks, brief, and synthetic sample policies, under the MIT license |

Questions after the conference are welcome. Email is the fastest way to reach me.

## What we build

Software development at ISK is a function inside the IT department: a small team of developers and a DBA that designs, builds, deploys, and hosts the agency's internal applications and data pipelines on its own infrastructure. Each project starts with a scoped request and an app owner, moves through requirements, code review, automated testing, and user acceptance, and runs in production on servers ISK operates. Every app is built on the same shared foundations, so each one ships faster than the last. This is what is running today.

| Product | What it does |
|---|---|
| **Lantern** | Runs the Quality Monitoring Review (QMR), ISK's annual audit of its contracted providers, and the Quarterly Record Review (QRR) of ISK's own programs: schedules, notices, scored review tools, findings and plans of correction, and the assembled reports |
| **Finance Requests** | Purchase requests for every ISK employee: a submission wizard, multi-tier approvals, receipt reconciliation, and an archival PDF of each request |
| **Ledger** | The Office of Recipient Rights registry of substantiated allegations, with every change audited, and next the ORR Review workspace for site visits, plans of correction, and staff training follow-up |
| **Ideas** | A quality improvement portal where staff submit and vote on suggestions and reviewers triage them |
| **Harbormaster** | A read-only portal where developers see container health, logs, usage, and the running version of the apps assigned to them, without production deploy access |
| **Vista** | In progress. Targeted utilization review: the review episodes for targeted clients, their follow-ups and appeals, and the data behind them |
| **Relay** | In progress. Employee change requests such as new hires, role changes, and terminations that fan out into tasks for HR, IT, Finance, and Security, with fulfillment tracked to completion |
| **Custom data pipelines** | Scheduled jobs, each in its own container: court and jail CSVs, CCBHC workbooks, vendor system exports, and Power BI tenant metadata into SQL Server, a payroll integration between two HR platforms, SQL Agent monitoring with alerts, and an appointment-to-Outlook calendar sync |

## ISK Standards

| Area | Practice |
|---|---|
| **Stack** | Python and Flask, htmx and Alpine, SQL Server. A shared library and component layer so every app starts from the same foundations. |
| **Source control** | One GitHub organization. A protected `main`, every change through a reviewed pull request, Conventional Commits, SemVer, squash merges. |
| **CI** | ruff, Semgrep, pip-audit, and the test suite run on every pull request. Red does not merge. |
| **Hosting** | Docker containers behind Traefik on ISK's own servers, deployed with Dockhand, with separate UAT and production environments behind the VPN. |
| **Protected information** | Synthetic data in development and test. Database error text is scrubbed before it is logged, logs are purged on a schedule, and production refuses to start with debug or SQL logging on. |
