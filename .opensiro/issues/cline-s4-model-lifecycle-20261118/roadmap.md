# cline/cline — Upstream #58 independent v0.18 receipt

- Receipt contract: proposal-gate
- Original repository: cline/cline
- Original HEAD: 20b042723a14412f6c1e84230b008708534d6e8c
- Observed at: 2026-11-19
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/cl/cline.md
- Accepted assessment blob SHA: 7dcc1f6f9e1087b867f2074549949d3dd26a9ced
- Accepted review ref: cfe9cadab99617d5013bf89f07b079d105057791
- Accepted reviewed at: 2026-09-15
- Accepted Index commit: c2e43bf4750841277b3e58d8ba80314121734764
- Accepted Profile version: 0.2.1
- Accepted Skills methodology version: 0.3.1
- Accepted VSM vector: S1=A · S2=C · S3=C · S3*=C · S4=— · S5=—
- System in focus: Cline first-party VS Code/SDK team runtime, provider/model catalogs, CLI Hub and supported client configuration; excluding provider vendors' release-governance decisions
- Matching working fork: opensiro-contributions/cline
- Fork owner control: ACTIVE/ALLOW per .opensiro/state.json
- Repository-wide source map: apps/vscode/src/sdk/model-catalog/catalog.ts; sdk/packages/core/src/extensions/tools/team/multi-agent.ts; docs/cli/agent-teams.mdx; original README, docs, tests, license, contributing, original Issues/PRs
- Evaluation object: Observed Hub→local→Hub upgrade inconsistency; an autonomous outside/future model-strategy owner does not repair that same current-state bug
- Existing-work overlap: First-party provider catalog refresh, cache TTL and operator-selected provider configuration; issue #15795 shows running Hub not restarted by upgrade, not future/environment adaptation demand; team already reviews outcomes
- Our on-top contribution: No additional native S4 C port justified. Correct the Hub upgrade restart and provider invalidation via existing architecture before proposing a model lifecycle control actor.
- Incremental benefit: none established against native current task; not measured
- Decision scope: one source-pinned proposed C capability, not whole-project or Index regrade
- Priority rationale: S1/S2/S3/S3* have existing native ownership where applicable; no source-backed unique lawful S4/S5 decision and feedback
- Target transition: NO_QUALIFIED_C_TARGET
- P1 dependencies: Reproduce and route native #15795 running-Hub restart correctness; check existing provider picker and catalog invalidation
- P2 optional: NONE
- Proposed C construction: No additional native S4 C port justified. Correct the Hub upgrade restart and provider invalidation via existing architecture before proposing a model lifecycle control actor.
- C sufficiency falsifier: A measured provider deprecation or capability-shift scenario proves native catalog refresh and legitimate manual switching cannot adapt future runs, while a new bounded autonomous S4 actor produces distinct permitted later-operation feedback
- Scenario basis: OBSERVED
- Proposal-stage decision: NO_GO
- Research disposition: NO_USEFUL_CHANGE
- Proposed validation: Reproduce stale Hub upgrade and verify restart semantics, compare model provider catalog cache reload against unchanged baseline; new S4 actor not warranted, NOT_RUN
- Validation state: NOT_RUN
- Proposal falsifier: A measured provider deprecation or capability-shift scenario proves native catalog refresh and legitimate manual switching cannot adapt future runs, while a new bounded autonomous S4 actor produces distinct permitted later-operation feedback
- Result: NO_USEFUL_CHANGE
- External issue: DRAFT — NOT PUBLISHED
- Public fork Issue: DRAFT — NOT PUBLISHED
- Cost status: NOT_MEASURED
- S1 disposition: first-party autonomous operational tasks under native tool feedback
- S2 disposition: optional team task board/mailbox provides composable coordination
- S3 disposition: optional team lead controls active teammates and commitments
- S3* disposition: reviewed/rejected fragments gate team outcome finalization
- S4 disposition: provider catalog refresh is not a developer-composed future environment decision owner
- S5 disposition: operator, deployment and user retain ultimate constraints

## Identity and pins

Pinned [Index assessment](https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/cl/cline.md), review [cfe9cadab99617d5013bf89f07b079d105057791](https://github.com/cline/cline/commit/cfe9cadab99617d5013bf89f07b079d105057791), indexed 2026-09-15, blob 7dcc1f6f9e1087b867f2074549949d3dd26a9ced, Profile 0.2.1, Skills 0.3.1. Original [current HEAD](https://github.com/cline/cline/commit/20b042723a14412f6c1e84230b008708534d6e8c) is distinct; no new Index grades. Source-first research preceded old case comparison.

## Rights and authority

Matching writable fork parent checked and owner-controlled `opensiro/meta` state ACTIVE/ALLOW read back. License/contributing assessed; CAMEL AI policy demands accepted discussion, human review and tests; Cline needs approved feature issue first. No public fork Issue, original Issue/comment/PR or product code authorized. Parent policy remains authoritative.

## Existing work / overlap

Source [apps/vscode/src/sdk/model-catalog/catalog.ts](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/apps/vscode/src/sdk/model-catalog/catalog.ts); [sdk/packages/core/src/extensions/tools/team/multi-agent.ts](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/extensions/tools/team/multi-agent.ts); [docs/cli/agent-teams.mdx](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/docs/cli/agent-teams.mdx). Native work [issues / 15795](https://github.com/cline/cline/issues/15795); [pull / 15796](https://github.com/cline/cline/pull/15796). First-party provider catalog refresh, cache TTL and operator-selected provider configuration; issue #15795 shows running Hub not restarted by upgrade, not future/environment adaptation demand; team already reviews outcomes. A new agent name alone is neither a source-grounded C nor permission for a product change.

## Function ownership

- **S1** historical **A**: first-party autonomous operational tasks under native tool feedback. NO_TARGET or DEFER.
- **S2** historical **C**: optional team task board/mailbox provides composable coordination. NO_TARGET or DEFER.
- **S3** historical **C**: optional team lead controls active teammates and commitments. NO_TARGET or DEFER.
- **S3*** historical **C**: reviewed/rejected fragments gate team outcome finalization. NO_TARGET or DEFER.
- **S4** historical **—**: provider catalog refresh is not a developer-composed future environment decision owner. NO_TARGET or DEFER.
- **S5** historical **—**: operator, deployment and user retain ultimate constraints. NO_TARGET or DEFER.

## Parallel contribution-on-top review

| Necessary function-specific outcome | Track A: shipped/Issue/PR | Track B: independent minimum addition or NONE | Falsifier |
| --- | --- | --- | --- |
| Observed Hub→local→Hub upgrade inconsistency; an autonomous outside/future model-strategy owner does not repair that same current-state bug | First-party provider catalog refresh, cache TTL and operator-selected provider configuration; issue #15795 shows running Hub not restarted by upgrade, not future/environment adaptation demand; team already reviews outcomes | No additional native S4 C port justified. Correct the Hub upgrade restart and provider invalidation via existing architecture before proposing a model lifecycle control actor. | A measured provider deprecation or capability-shift scenario proves native catalog refresh and legitimate manual switching cannot adapt future runs, while a new bounded autonomous S4 actor produces distinct permitted later-operation feedback |
| Later operational closure and parent rights | Real native task/host feedback, license and parent authority | Existing native defect repair, configuration and user control are the baseline; no autonomous S4 | Same result without distinct owner or without lawful enforcement |

## Capability priority

P0: NO_QUALIFIED_C_TARGET. P1: Reproduce and route native #15795 running-Hub restart correctness; check existing provider picker and catalog invalidation. P2: NONE. Research **NO_GO/NO_USEFUL_CHANGE**. The historical states are not a defect checklist.

## Implementation options

No additional native S4 C port justified. Correct the Hub upgrade restart and provider invalidation via existing architecture before proposing a model lifecycle control actor.. Compare simpler alternative First-party provider catalog refresh, cache TTL and operator-selected provider configuration; issue #15795 shows running Hub not restarted by upgrade, not future/environment adaptation demand; team already reviews outcomes. Proposed C requires eligible inputs, decisive actor, lawful enforcement, actual later operation and returned feedback; none is qualified above existing controls for this observed problem. Falsifier: A measured provider deprecation or capability-shift scenario proves native catalog refresh and legitimate manual switching cannot adapt future runs, while a new bounded autonomous S4 actor produces distinct permitted later-operation feedback.

## Specification and domain alternatives

Earlier Cline roadmap was NEEDS_EVIDENCE on hypothetical S4 model lifecycle; this narrower current-head independent rerun finds no qualified C for the observed Hub route.. Original authors own implementation; historical different case did not determine this first-pass outcome. Missing S4/S5 code does not imply a deliberate omission; intention UNVERIFIED. No Profile/Skills changes implied.

## Cost experiment

Matched native comparator: Reproduce stale Hub upgrade and verify restart semantics, compare model provider catalog cache reload against unchanged baseline; new S4 actor not warranted, NOT_RUN. Measure correct decisions, reviewer/regression effort, latency, tokens, human approval and maintenance cost. NOT_RUN; NOT_MEASURED.

## Delivery and publication

[Human](issue.md) and [AI](constructor-sufficiency.md) derive this **NO_GO/NO_USEFUL_CHANGE**. Internal OpenSiro fork metadata only; external issue DRAFT — NOT PUBLISHED. Current Index and original product untouched. No native tests, CI or cost measurements asserted.
