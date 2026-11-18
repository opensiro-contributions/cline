# Cline — source-native S4 capability roadmap receipt

## Identity and pins

- Original repository: cline/cline
- Original HEAD: eff43e19b267e171f597ab03733bfed25090f72d
- Observed at: 2026-11-18
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/5f6ea0c777733813ca42e3f210390a719488dcfb/assessments/cl/cline.md
- Accepted assessment blob SHA: 7dcc1f6f9e1087b867f2074549949d3dd26a9ced
- Accepted review ref: cfe9cadab99617d5013bf89f07b079d105057791
- Accepted reviewed at: 2026-09-15
- System in focus: first-party SDK/CLI hub scheduled-agent mode and shared provider catalog; outside external providers, maintainers, VS Code-only surface, private services
- Historical full vector: S1=A / S2=C / S3=C / S3*=C / S4=— / S5=—; Profile 0.2.1 / Skills 0.3.1
- Latest accepted semantic check: 2026-09-17 (62 days before observation); Index reassessment advised, not a plan-only blocker
- Result: NEEDS_EVIDENCE
- Case ID: cline-s4-model-lifecycle-20261118
- Working fork: https://github.com/opensiro-contributions/cline

## Rights and authority

- License: [Apache-2.0](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/LICENSE); [CONTRIBUTING.md](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/CONTRIBUTING.md) requires issue and maintainer approval before a feature PR; no CLA claim beyond the stated contribution agreement.
- Verified fork parent: cline/cline; fork owner push rights observed. New meta initializes restrictive DORMANT/PAUSE rather than inventing owner ALLOW. This research plan does not require product code.
- Legitimate parent/human retains policy/model credential and schedule ownership; a proposed developer actor may decide only within delegated, first-party supported scope. No claim of current S4=C or S5 ownership.

## Existing work / overlap

- SHIPPED: [ModelInfo metadata](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/shared/src/llms/model-info.ts), [live catalog config](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/llms/src/providers/config.ts), [explicit schedule model selection](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/apps/cli/src/commands/schedule/model-selection.ts), [schedule update/pause](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/core/src/cron/service/schedule-tool.ts), [persistent runs](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/core/src/cron/service/schedule-service.ts).
- OPEN ISSUES (2026-11-18): [#15446](https://github.com/cline/cline/issues/15446) variant metadata; [#15481](https://github.com/cline/cline/issues/15481) actual routing vs displayed price; [#13921](https://github.com/cline/cline/issues/13921) API incompatibility. They do not prove schedule adaptation demand.
- OPEN PRs: [#12357](https://github.com/cline/cline/pull/12357) provider capabilities and [#15670](https://github.com/cline/cline/pull/15670) settings. MERGED PR: [#15499](https://github.com/cline/cline/pull/15499) token budget. Avoid duplicate implementation.
- UNVERIFIED: whether an existing SDK/plugin path plus schedule API already provides developer-owned model adaptation and feedback, and how schedule auth/run-model correlation behaves end to end. No code or native test run performed.

## Function ownership

- S1 operational scheduled coding/maintenance tasks. S2/S3/S3* C states are from the historically assessed opt-in team mode and do not automatically credit this scheduled mode.
- S4 proposed: externally dated model change → credible future options → developer-composed autonomous selection → authorized future schedule update/hold → observed later run and feedback to current S3. Current data transport and model metadata alone do not close S4.
- S5 reserved ultimate identity/policy authority remains with legitimate parent; a budget/safety gate is not a S5 agent.
- Falsifier: if existing native configuration/plugins already provide an equally useful lawful path, do not add a new constructor.

## Capability priority

- P0: **conditional S4=C construction** for developer-owned selection of a supported replacement or hold for future recurring run, tied to next-run receipt.
- P1: prove real operator need, check existing composition/overlap and provider trust, enforce workspace/schedule permissions, correlate run/model feedback, add native tests. P1 may precede P0.
- P2: **NONE**; no forced secondary S3/S5 enhancement.
- Sufficiency: five *logical* ports A signal, B options, C developer decision actor, D authorized schedule transition, E next-run receipt; absent any link, no constructor claim. Full native acceptance in [AI contract](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/constructor-sufficiency.md).

## Implementation options

- Preferred low-cost baseline: manual operator model verification and supported schedule configuration update/hold, then inspect next run. Measure if this already solves the task.
- If need and integration are proven: minimal first-party opt-in S4 decision-to-schedule bridge; no new model facts registry, unrelated agent hierarchy, or background network daemon required by this plan.
- Proposed tests: real next-run substitution, alternative hold, invalid rights/stale facts rejection, provider-error feedback, opt-out behavior and baseline comparison. **NOT EXECUTED**.

## Specification and domain alternatives

- Original-native roadmap/PR only with source project maintainer preapproval and separate OpenSiro permission; optional Profile/Skills method feedback solely if semantically evidenced; independent domain fork only under separate legal/authority check.
- Original issue is a distinct public action, not authorized by this case. External maintainer acceptance is not transferred.

## Cost experiment

- Matched task: scheduled job needs different provider/model after real upstream change. Compare manual configuration with opt-in developer-composed adaptation on same authority, timing and eligible models. Track operator effort, code + integration + review + testing + maintenance, failures and quality.
- Cost status: NOT_MEASURED

## Delivery and publication

- Human Issue draft: [issue.md](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/issue.md); technical constructor and acceptance: [constructor-sufficiency.md](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/constructor-sufficiency.md); case readme: [README.md](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/README.md).
- Fork GitHub Issue: READY_FOR_FORK_ISSUE_APPROVAL — NOT PUBLISHED (separate exact current-conversation title/body approval required).
- External issue: DRAFT — NOT PUBLISHED
- Product implementation: NONE; original Issue / PR: NOT PUBLISHED; Index regrade: NONE.
- Owner control on new meta: DORMANT/PAUSE, not an automatic RESUME.
