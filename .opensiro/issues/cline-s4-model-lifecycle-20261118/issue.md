# Cline — proposed future model-transition intelligence for Hub schedules (Human Roadmap)

**Target transition:** S4=— -> S4=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

**PLAN_ONLY · HYPOTHETICAL · original product UNCHANGED · public Issues/PRs NOT PUBLISHED**

**One-sentence construction:** Enable an optional Cline agent to assess dated future provider/model changes for a **specific recurring Hub schedule**, autonomously select *retain / migrate / hold*, and let the parent user authorize the existing interactive schedule update; subsequent execution results return to the S4 investigator. This is **not** an agent secretly switching users' models.

**Canonical source of truth:** [roadmap.md](roadmap.md) — pins, six-function dispositions, research/validation and decision. **Technical implementation/falsifier:** [constructor-sufficiency.md](constructor-sufficiency.md). Stable case on `opensiro-contributions/cline@opensiro/meta:.opensiro/issues/cline-s4-model-lifecycle-20261118/`.

## Central accepted historical VSM assessment

Historical accepted Index (not a current-HEAD regrade): **S1=A · S2=C · S3=C · S3*=C · S4=— · S5=—**. [Included assessment pinned at 41ce688](https://github.com/opensiro/vsm-harness-index/blob/41ce68817f37a49158dceddf5d384863d54b4ee0/assessments/cl/cline.md), blob 7dcc1f6f9e1087b867f2074549949d3dd26a9ced, review ref cfe9cadab99617d5013bf89f07b079d105057791, 2026-09-15, Profile 0.2.1/Skills 0.3.1. Current original [source HEAD](https://github.com/cline/cline/commit/20b042723a14412f6c1e84230b008708534d6e8c), checked 2026-11-20. Later Profile 0.2.4 is normative, not a retroactive grade change.

| Function / plain-language role | Historical Index state | Current first-party owner/return | Candidate and priority |
| --- | --- | --- | --- |
| **S1 · Operations** | A | Autonomous coding and scheduled task model/tool loops act and observe outcomes | NO_TARGET |
| **S2 · Coordination** | C | Optional team mailbox/tasks/dependencies coordinate peer work and conflicting commitments | NO_TARGET |
| **S3 · Current regulation** | C | Optional team lead controls current commitments; Hub schedule state/interactive host controls active scheduled settings | NO_TARGET; recipient of S4 option |
| **S3* · Independent audit** | C | Optional independent reviewer and reviewed outcome fragments gate finalization | NO_TARGET |
| **S4 · Future/environment** | — | Model catalogue exposes status, but no autonomously owned external future option/return loop evidenced | **P0**: scheduled-task S4 constructor |
| **S5 · Ultimate policy** | — | User/developer reserves permissions and ultimate identity, not delegated by a cron tool | NO_TARGET |

Repository screen covered SDK, Core Hub/cron, CLI schedule commands, VS Code/Desktop provider settings and cloud restriction, optional teams/plugins, original tests, Issues/PRs and [CONTRIBUTING](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/CONTRIBUTING.md). Provider-company decisions and repository CI are outside this product boundary. A missing grade is not a defect; no intentional omission is asserted without evidence. Accepted states are autonomy categories, not quality ranking.

## Specific developer/operator scenario

A recurring Cline Hub schedule uses provider **P** / model **M**. An externally verifiable dated notice forecasts retirement/compatibility changes. The optional S4 investigator compares available models and selects between **retain, migrate candidate, hold** for **that schedule_id**, recording the source and expiry. The user can approve the candidate **in an interactive session**; only then the built-in `tasks.scheduled` **update** takes `model_selection`. A later scheduled execution should use the updated provider/model and publish a result that can inform the investigator. This scenario is HYPOTHETICAL; no real impending provider sunset or maintainer demand is claimed.

**What Cline already supports (Track A):** [`tasks.scheduled` tool](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/service/schedule-tool.ts) accepts interactive, workspace-scoped `update` with `model_selection`; **it rejects noninteractive mutations**. [`HubScheduleService.updateSchedule`](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/service/schedule-service.ts) persists model settings; [`CronRunner.buildStartRequest`](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/runner/cron-runner.ts) uses stored `providerId/modelId` for future runs and publishes completion/failure events. [Core scheduled agents](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/docs/sdk/guides/scheduled-agents.mdx) and [live model catalogue](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/llms/src/catalog/catalog-live.ts) are reusable. The built-in [schedule execution listing](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/service/schedule-service.ts) reports `executionId/sessionId/status` but not a standalone immutable actual-model receipt for the S4 investigator.

**What to construct (Track B):** an optional, dated-source S4 analysis/proposal for `schedule_id`; reuse the **existing** user-interactive task update rather than inventing another general Host write API; verify/complete a *read-only* association between accepted proposal, next schedule revision, actual run model and completion/failure, using existing history/session data where possible. Do not bypass the noninteractive guard to make a stronger demo.

| Required S4 chain | Native A | Smallest missing original-native B |
| --- | --- | --- |
| External future model distinction and choice | Catalogue + cron/agents | Dated notice, alternatives and autonomous retain/migrate/hold decision for one schedule |
| Legitimate change to future operation | Workspace-checked interactive `tasks.scheduled.update` and persisted `modelSelection` | Proposal attached to specific schedule, explicit parent approval; **no headless mutation** |
| Future-run feedback | CronRunner run events + Hub schedule execution history/sessionId | Prove actual executed model and correlate result to approved proposal; add only minimal read-only projection if necessary |

**P0:** S4 future-option owner → interactive authorized native schedule change → later-run result to S4. **P1:** dates/compatibility, workspace/parent rights, actual-model/run correlation and no race with in-flight run. **P2:** NONE. **Proposed C-sufficiency:** GO at proposal stage only, with NEEDS_EVIDENCE for unexecuted native tests. A user may simply switch models manually; the decision whether to add this is Cline maintainers', not OpenSiro's.

## Patch refinement, validation and handoff

The initial v0.18.0 [independent GO seal](https://github.com/opensiro/upstream/issues/58#issuecomment-7043170806) remains unchanged. The v0.18.1 [native-specific PATCH](https://github.com/opensiro/upstream/blob/main/changes/v0.18.1.md) is advisory and adds no test/acceptance metric. It revealed the earlier proposed *generic new typed Host port* was too broad: Cline's existing `tasks.scheduled.update` already has an authorized path. This case therefore narrows P0 to Cline **Hub schedules**, with explicit guard/feedback.

Earlier [2026-11-19 NO_GO](https://github.com/opensiro-contributions/cline/commit/3437b3be25df2404b19cc699a52590a46bbc6e0f) evaluated a current Hub restart bug (#15795), not prospective scheduled model transitions. Preserved in immutable Git history; this continuation is not an independent new run.

**Future acceptance (NOT_RUN):** two externally dated scenarios yield different prospective options; interactive and correct-workspace approval updates only the named schedule; the subsequent execution really uses the approved model and returns its status; stale/unsupported input, cross-workspace access and noninteractive mutation fail safely; an already-running run does not switch mid-flight. The original [schedule-tool tests](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/service/schedule-tool.test.ts), [schedule-service tests](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/service/schedule-service.test.ts) and [cron-runner tests](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/runner/cron-runner.test.ts) are the native test anchors. **Falsifier:** no distinct prospective choice, no lawful later action, or no reliable returned actual-run information.

Rights: fork `ACTIVE/ALLOW` covers internal .opensiro files, not third-party GitHub publications. Original product and accepted Index unchanged; native behavioral tests NOT_RUN, cost/benefit NOT_MEASURED. No extra Upstream run PR: [#84 closed unmerged](https://github.com/opensiro/upstream/pull/84), preserved in the single [Supplementary report](https://github.com/opensiro/upstream/blob/main/docs/ROADMAP_REPORT.md#supplementary). AI-assisted proposal, not an authorized implementation.
