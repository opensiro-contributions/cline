# Cline — Upstream #58 Wave 4, v0.18.1 native-specific continuation

- Receipt contract: proposal-gate
- Original repository: cline/cline
- Original HEAD: 20b042723a14412f6c1e84230b008708534d6e8c
- Observed at: 2026-11-20
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/41ce68817f37a49158dceddf5d384863d54b4ee0/assessments/cl/cline.md
- Accepted assessment blob SHA: 7dcc1f6f9e1087b867f2074549949d3dd26a9ced
- Accepted review ref: cfe9cadab99617d5013bf89f07b079d105057791
- Accepted reviewed at: 2026-09-15
- Accepted Index commit: 41ce68817f37a49158dceddf5d384863d54b4ee0
- Accepted Profile version: 0.2.1
- Accepted Skills methodology version: 0.3.1
- Accepted VSM vector: S1=A · S2=C · S3=C · S3*=C · S4=— · S5=—
- System in focus: First-party Cline SDK/CLI/Core Hub scheduled-agent runtime with its workspace-scoped task tool, provider catalogue and user/parent policy; VS Code/desktop/opt-in teams considered in six-function census but not presumed automatically supported by this P0
- Matching working fork: opensiro-contributions/cline
- Fork owner control: ACTIVE/ALLOW, opensiro/meta; permits only internal OpenSiro case metadata
- Repository-wide source map: README, CONTRIBUTING, sdk/ARCHITECTURE, sdk/packages/core/src/ClineCore.ts and cron/service/schedule-tool.ts, schedule-service.ts, schedule-command-service.ts, cron/runner/cron-runner.ts, apps/cli/src/commands/schedule/model-selection.ts, llms/catalog/catalog-live.ts, apps/vscode/src/sdk/model-catalog/catalog.ts and store.ts, sdk plugin/scheduled-agent/team docs, tests and original Issues/PRs
- Evaluation object: Developer-composed S4 prospective provider/model transition for a particular Cline Hub recurring schedule, with interactive user-authorized schedule model change and later scheduled-run feedback; not generalized runtime self-modification
- Existing-work overlap: Existing tasks.scheduled update takes model_selection, rejects noninteractive session mutations and checks workspace scope; HubScheduleService.updateSchedule persists modelSelection; CronRunner.buildStartRequest consumes the saved provider/model; schedule.execution completed/failed and listScheduleExecutions give run status/sessionId but not an explicit immutable executed-model receipt to the S4 owner
- Our on-top contribution: Optional scheduled S4 research agent produces a dated externally evidenced retain/migrate/hold proposal for one schedule; reuse interactive tasks.scheduled update for approved change and existing schedule execution events/history, adding only a small proposal-to-run correlation/read-only feedback adaptation if evidence shows needed; no generic Host transition-port or noninteractive mutation bypass
- Incremental benefit: HYPOTHETICAL: earlier informed model transition of a recurring task and verifiable later-run outcome; product desirability, accuracy and cost NOT_MEASURED
- Decision scope: Source-native proposed S4=C constructibility for scoped scheduled tasks; not shipped, not a maintainer choice, not a general automatic model-changing capability or Index reassessment
- Priority rationale: S1 A and optional team S2/S3/S3* C already have first-party paths; S4 distinct prospective dated notices, autonomous option choice and return to current Hub schedule operations are architecturally composable; ultimate permissions stay with parent S5
- Target transition: S4=— -> S4=C
- P1 dependencies: Prove actual dated external signal provenance, alternative model eligibility and workspace scope; interactive approval at tasks.scheduled update, no headless update; correlate a particular proposal to returned schedule revision and actual provider/model in the subsequent run, plus history/error feedback; test race with active run and reject stale or revoked authorization
- P2 optional: NONE
- Proposed C construction: Compose a Cline scheduled agent to inspect dated model sunset/capability notices against current llms catalogue and a named Hub schedule; its autonomous retain/migrate/hold choice becomes an auditable proposal; parent-approved interactive tasks.scheduled update writes model_selection through HubScheduleService; CronRunner subsequently starts with persisted provider/model; correlate subsequent schedule.execution event/listScheduleExecutions and actual session provider/model back to S4 for revising next options
- C sufficiency falsifier: The proposed investigator only parrots deprecated metadata or makes no independent prospective choice; no lawful interactive change can reach a later Hub run; no reliable actual run outcome/model can return; or equivalent S4 future-choice and feedback is already first-party closed
- Scenario basis: HYPOTHETICAL
- Proposal-stage decision: GO
- Research disposition: NEEDS_EVIDENCE
- Proposed validation: Native schedule-tool.test.ts interactive update success and noninteractive refusal, workspace/parent veto, model_selection forwarding; schedule-service.test.ts persistence; cron-runner.test.ts actual next-run model and event/session correlation; stale/invalid notice and in-flight run invariants; all NOT_RUN
- Validation state: NOT_RUN
- Proposal falsifier: Cannot close S4 future option → lawful current schedule change → actual later run with a distinguishable outcome while respecting noninteractive and parent boundaries
- Result: NEEDS_EVIDENCE
- External issue: DRAFT — NOT PUBLISHED
- Public fork Issue: DRAFT — NOT PUBLISHED
- Cost status: NOT_MEASURED
- S1 disposition: Historical A; first-party coding/cron agents produce tool-validated operational outcomes; not a C target
- S2 disposition: Historical C; optional teams provide mailbox/shared tasks and actual conflict attenuation; not a C target
- S3 disposition: Historical C; optional team coordinator and current Hub schedule state regulate current commitments; S4 plan requires lawful operator/host effect
- S3* disposition: Historical C; optionally composed independent outcome reviewer can gate completion, distinct from ordinary cron success logs
- S4 disposition: Historical —; catalog lists model status but no verified autonomous prospective notice-to-choice-to-run-feedback owner; narrowly proposed schedule-native P0
- S5 disposition: Historical —; model permissions, schedule edit consent and final identity remain human/developer or parent; do not construct a policy authority

## Identity and pins

This is a **continuation / refinement**, not a new independent Wave 4 first pass. The source-first v0.18.0 [GO + NEEDS_EVIDENCE seal](https://github.com/opensiro/upstream/issues/58#issuecomment-7043170806) and the [2026-11-19 historical NO_GO](https://github.com/opensiro-contributions/cline/commit/3437b3be25df2404b19cc699a52590a46bbc6e0f) remain immutable provenance. Recheck original [HEAD](https://github.com/cline/cline/commit/20b042723a14412f6c1e84230b008708534d6e8c), historical [included Index](https://github.com/opensiro/vsm-harness-index/blob/41ce68817f37a49158dceddf5d384863d54b4ee0/assessments/cl/cline.md), released [v0.18.0](https://github.com/opensiro/upstream/releases/tag/v0.18.0) and integrated **v0.18.1 advisory** [native-specific recommendation](https://github.com/opensiro/upstream/blob/main/changes/v0.18.1.md). The v0.18.1 patch adds no new GO/NO_GO gate or grade; its recommendation prompted replacement of an unnecessary generic transition-port assumption with specific Cline schedule mechanisms.

## Rights and authority

Source fork is verified opensiro-contributions/cline, parent cline/cline, Apache-2.0; opensiro/meta state ACTIVE/ALLOW authorizes case updates, not product implementation. [CONTRIBUTING.md](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/CONTRIBUTING.md) requires maintainer-approved feature request before implementation. Explicit Cline safety constraint: [tasks.scheduled](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/service/schedule-tool.ts) rejects **all schedule mutation** from noninteractive sessions and enforces matching workspace scope. A background S4 task may only produce a proposal; a legitimate user/parent-bound interactive session must apply any allowed update. No invented standing permission, no quiet model rewrite, no current-session or running cloud-session mutation. Original and public-fork GitHub publication separately requires exact approval.

## Existing work / overlap

First-party [Cline Core automation](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/ClineCore.ts) and [scheduled agents](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/docs/sdk/guides/scheduled-agents.mdx) launch persistent recurring work. [Live catalogue](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/llms/src/catalog/catalog-live.ts) has status/deprecation filtering but no dated future notice/strategy owner. The [schedule task](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/service/schedule-tool.ts) supports `{operation: "update", schedule_id, model_selection: {provider_id, model_id}}`, validates interactive status and workspace; [Hub command](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/service/schedule-command-service.ts) also supports schedule.update with modelSelection. [HubScheduleService](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/service/schedule-service.ts) already persists update and exposes listScheduleExecutions with executionId/sessionId/status; [CronRunner.buildStartRequest](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/cron/runner/cron-runner.ts) reads `spec.providerId` and `spec.modelId` when starting the next run and publishes completion/failure events, **but** the event payload omits the executed model. CLI [resolveScheduleModelSelection](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/apps/cli/src/commands/schedule/model-selection.ts) accepts explicit provider/model for creation; CLI `schedule history` is a native feedback alternative. In regular VS Code, buildSessionConfig has a runtime override, but it is documented for the cloud session path and is **not** a general authorization to mutate user model selection. Original issues/PRs about Hub restart (#15795), catalog refresh (#15667) and model settings (#15670/#15677) are separate native context, not equivalent prospective S4 closure.

## Function ownership

- **S1 / A:** agent tool execution adapts to code/environment feedback; no missing S1 functionality posited.
- **S2 / C:** optional first-party team mailboxes/dependencies help prevent interference among distinct workers; not an S4 substitute.
- **S3 / C:** optional team coordinator owns present assignments; HubScheduleService owns deterministic current schedule state. A legitimate interactive owner approves changes affecting upcoming operations.
- **S3* / C:** optional independent reviewer judges reviewable outcome fragments; merely checking schedule success is not independent audit.
- **S4 / —:** dated external future provider changes, option selection and later-run feedback are **not** a shipped autonomous function; S4 candidate restricted to a named recurring schedule.
- **S5 / —:** parent user owns ultimate model/permission policy. No inference of deliberate omission without evidence; no score or imposed six-function quota.

## Parallel contribution-on-top review

| S4 link | Track A — existing first-party | Track B — minimal on-top native construction | Falsifier |
| --- | --- | --- | --- |
| Externally prospective difference | `llms/catalog-live.ts` status/deprecated and Core cron | Optional scheduled S4 research prompt/tool reading dated external provider notices with provenance, eligible alternatives for one `schedule_id` | Only current catalog refresh or fabricated sunset |
| Autonomous alternative choice | Session prompt/agent loop and existing model metadata | S4 agent chooses *retain/migrate/hold*, emits reasoned versioned proposal; does **not** call mutating scheduled_task in its own headless session | Choice only a static warning or hardcoded model |
| Lawful current effect | `schedule-tool.ts` interactive/workspace-gated `update` and `schedule-service.ts` persistence | Human/parent interactive accepts specific schedule+model proposal using **existing** `tasks.scheduled.update`; avoid new general Host mutation port | Requires bypassing noninteractive guard or wrong workspace |
| Later operation and return | `cron-runner.ts` starts with schedule model; `schedule-service.ts.listScheduleExecutions` returns execution status/sessionId; events emitted | Correlate approved proposal, schedule revision and **actual** run model/outcome into S4 next observation, using existing history/session lookup where proven; only if needed add schedule-local read-only history/proposal reference | Scheduled run uses different model, or status not attributable to proposal |

## Capability priority

**P0:** one named Cline schedule: externally sourced prospective change → autonomous, documented retain/migrate/hold choice → parent-approved interactive schedule update → future-run result returned to S4. **P1:** prove reliable proposal/run identity join and read-only history path, parent/workspace restrictions, candidate eligibility, active-run version boundary and falsification. **P2:** NONE. The initial generic full-product typed Host bridge is **withdrawn as unnecessary for this narrower native design**. This advisory tightening does not change the scoped GO/NEEDS_EVIDENCE verdict or prove the user needs the feature.

## Implementation options

**Native operator alternative (cheapest):** the owner sees deprecation in the catalog, manually updates the same recurring task's model with current `tasks.scheduled` or CLI, then checks `cline schedule history`. This is legitimate and may be preferred by Cline maintainers. **Not sufficient for distinct autonomous S4:** a scheduled alert alone has no autonomous choice or closed returned later-run effect. **Narrow source-native C construction:** use existing `ClineCore.automation` to run opt-in future notice analysis; S4 agent chooses among permitted, catalog-supported models; schedule result includes evidence, `schedule_id`, current and proposed provider/model and expiry. A separate **interactive** parent-approved invocation of existing `tasks.scheduled.update` persists `model_selection`. Core `CronRunner.buildStartRequest` consumes new model for a subsequent schedule run. Native history provides `executionId/sessionId/status`, and a minimal owner-scoped read-only correlation of actual selected model + proposal reference (if existing session lookup does not already suffice) feeds S4's next analysis. No automatic schedule mutation from a headless session and no speculative bespoke S5. Counterfactual: without the prospective choice-maker native scheduling still works, but source-driven alternative selection and corrective feedback no longer exist.

## Specification and domain alternatives

The previous Cline v0.18.0 Wave 4 [GO + NEEDS_EVIDENCE receipt](https://github.com/opensiro-contributions/cline/commit/e6a12a8fba0bfe7399c5e00cfc3f818f05e6940b) proposed a generic typed host model-transition port. Under the v0.18.1 **advisory** native-specificity patch, this continuation retains the same scoped verdict but **narrows the research target to Hub recurring schedules** and reuses existing `tasks.scheduled.update`, `HubScheduleService` and `CronRunner`. The earlier 2026-11-19 NO_GO addressed [Hub upgrade/restart bug #15795](https://github.com/cline/cline/issues/15795), not future S4. That prior result and the independent v0.18.0 first-pass seal are preserved in history; this continuation is not mislabelled a second independent attempt. Parent product decisions are never inferred, and no current Index regrade is proposed.

## Cost experiment

Matched scenario: same credible future model deprecation notice, one recurring Cline Hub task, valid alternative models. Compare human-only selection/update/history vs optional composed S4 proposal plus interactive approval and verified next-run result. Measure correctness of the action and model actually used, review/approval time, wrong-model incidents, tokens/latency and maintenance burden. **NOT_RUN / NOT_MEASURED**, no demonstrated product value.

## Delivery and publication

Human [issue.md](issue.md) and AI [constructor-sufficiency.md](constructor-sufficiency.md) derive from this canonical receipt. Original source code and Index remain unchanged. This is internal fork-local metadata only; structural validation must be read back, native/functional tests are NOT_RUN, GO is proposal-stage only. Upstream [PR #84](https://github.com/opensiro/upstream/pull/84) is closed unmerged and listed in the single [Supplementary navigation](https://github.com/opensiro/upstream/blob/main/docs/ROADMAP_REPORT.md#supplementary); no new per-run Upstream file/PR. Update the existing [coordination issue #58](https://github.com/opensiro/upstream/issues/58) with concise closure links; no third-party GitHub Issue/comment/PR or product implementation authorized.
