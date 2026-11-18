# Cline — developer-composable S4 model-lifecycle adaptation: conditional constructor and acceptance

**Level 2 / AI–developer contract · PLAN_ONLY / NEEDS_EVIDENCE · DRAFT — NOT PUBLISHED.** [Human decision Issue](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/issue.md) · [receipt](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/roadmap.md). The same historical vector and priorities apply: **S1=A · S2=C · S3=C · S3*=C · S4=— · S5=—**; **P0=S4, P1=evidence + scoped ports, P2=NONE**.

## Boundary and decision owner

Cline original `eff43e19b267e171f597ab03733bfed25090f72d`, accepted [Index](https://github.com/opensiro/vsm-harness-index/blob/5f6ea0c777733813ca42e3f210390a719488dcfb/assessments/cl/cline.md) (assessment blob `7dcc1f6f9e1087b867f2074549949d3dd26a9ced`, reviewed 2026-09-15 at `cfe9cadab99617d5013bf89f07b079d105057791`, Profile 0.2.1 / Skills 0.3.1). **These are historical grades, not current HEAD grades.** The target supported mode is first-party SDK/CLI hub scheduled-agent execution, not external GitHub maintenance, VS Code feature-only paths, provider intelligence, cloud policy or a generically claimed team-mode S3. Mode-level authority remains subject to first-party schedule scope and human/operator rules.

**S4 stimulus:** externally sourced model retirement, metadata drift or capability/price policy change before a future scheduled agent run. **S4 decisive owner (proposed, not shipped):** independently configured developer-supplied decision actor considers actual eligible future options (retain / hold / approved replacement) and may propose a transition. **Enforcement:** first-party scheduler/provider compatibility and scope; these are not themselves the decision owner. **Return:** only an authorized modification visible to the *next* schedule execution, paired with actual model/run feedback, closes the function. **S3↔S4:** report present schedule commitments, time/budget and conflicts into option evaluation; return lawful adapted configuration and actual run result to current control. Ultimate identity/policy stays with legitimate parent, no S5 invention.

## Current original-native primitives and overlap

| Pin | SHIPPED source fact or existing tracker | S4 sufficiency observation |
| --- | --- | --- |
| [ModelInfo schema](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/shared/src/llms/model-info.ts) | Model status (`active/preview/deprecated/legacy`), `replacedBy`, `deprecationDate`, capabilities, pricing | Data model only: no autonomous prospective choice |
| [Provider catalog config](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/llms/src/providers/config.ts) and [package guidance](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/llms/AGENTS.md) | Optional live catalog refresh and models.dev truth; guidance forbids a broad duplicate Cline-maintained registry | Reuse facts; don't add shadow registry |
| [Schedule model selection](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/apps/cli/src/commands/schedule/model-selection.ts) | Explicit provider+model or persisted last-used/default settings | At creation, configuration selection; not S4 future adaptation |
| [Schedule tool](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/core/src/cron/service/schedule-tool.ts) | `create/update/list/get/pause/resume/delete/run_now`, validated `model_selection`, workspace scope | Existing authorized operation surface; inspect ownership and per-run semantics |
| [Schedule service](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/core/src/cron/service/schedule-service.ts) | Durable schedule specs, planned modelSelection, execution status; actual run results | Need evidence of chosen model in returned run receipt and feedback to decision owner |
| [Original issues #15446](https://github.com/cline/cline/issues/15446), [#15481](https://github.com/cline/cline/issues/15481), [#13921](https://github.com/cline/cline/issues/13921) | OPEN: current model metadata/routing can differ from provider capabilities or price expectations | Real external data disturbance, **not** validated scheduled-agent demand |
| [PR #12357](https://github.com/cline/cline/pull/12357) and [#15670](https://github.com/cline/cline/pull/15670) | OPEN related model capabilities/settings changes; PR [#15499](https://github.com/cline/cline/pull/15499) MERGED | Do not duplicate their implementation or treat open PR as shipped |

**Evidence gap:** verify actual feature demand for automated future schedule adaptation, whether shipped SDK plugins or existing schedule update APIs can already supply the complete developer decision/return, and runtime denial paths. No exhaustive code claim is made. If equivalent existing native composition works, `NO_USEFUL_CHANGE`.

## Conditional minimum first-party S4 construction ports (not implemented)

| Logical port | Input → output | Owner/right | Reuse versus missing |
| --- | --- | --- | --- |
| **A · ModelLifecycleSignal** | Fresh timestamped catalog status/deprecation/capability delta with provider source + previous snapshot | Sensing is not S4 judgment | Reuse model catalog/ModelInfo; versioned per-schedule comparison unverified |
| **B · ScheduleAdaptationOptions** | Schedule ID, original model, eligibility/credentials, current commitments, `retain/hold/replacement`, expiry | No unsupported or unauthorized proposal | Reuse scheduler and catalog; admissible option-case generation unverified |
| **C · ModelAdaptationDecision** | Developer supplies agent/evaluator selecting lawful future option with principal, reason and option version | **Proposed composable decisive S4 owner** distinct from hardcoded validator | Scoped SDK actor wiring unverified; no default automatic policy |
| **D · AuthorizedScheduleTransition** | Valid choice → first-party `updateSchedule` or `pauseSchedule` affecting only future runs; no mutation of active sessions | Scheduler/human scope and credential gate; preserve parent rights | Reuse existing update/pause; adapter and race/rollback semantics unverified |
| **E · NextRunAdaptationReceipt** | Actual later run uses chosen provider/model, records execution ID, failure or success, sends feedback to decision owner / current commitments | Demonstrated returned effect, not an intent/log alone | Reuse schedule execution records; chosen-model evidence correlation unverified |

**Conditional sufficiency:** only if all five ports are reachable in the supported distribution; developer's independent actor actually chooses between valid alternatives; a scoped native operation obeys rights and changes subsequent behavior; a real receipt returns. A generic hook, catalog change, deterministic fallback, external cron script or human-only settings edit alone does **not** establish new S4=C. Nothing here changes the accepted Index.

## Construction sequence / proposed native test contract

**P1A.** Confirm a willing scheduled-agent operator's concrete model-change problem, exact native workaround and whether direct composition with existing plugin/schedule API already solves it. Record versions and user-visible outcomes. Require repo-native code/tests before implementation.  
**P1B.** Verify model variant metadata, trusted catalog timestamp, schedule ID ownership, credentials, existing run idempotency, and source-native baseline failures; avoid duplicate model registry.  
**P1C.** Only if qualified, add minimal opt-in async decision and scoped schedule transition in existing first-party SDK/hub path, not a separate service or authority transfer.  
**P0.** Complete decision → subsequent run → feedback, demonstrate a materially improved operator task.  
**P2: NONE — no additional constructor.**

**Proposed, NOT EXECUTED, acceptance scenarios derived from the pinned scheduler/catalog:**

1. **S4-POSITIVE.** Given recurring schedule X using a catalog-deprecated model, a developer-provided actor reviews retained/held/replacement options, selects an eligible replacement, and after an authorized update the *next* run of X records the replacement model and actual execution status. Neither a UI banner nor a proposed update passes.
2. **S4-ALTERNATIVE.** Given the same trusted source change and same X, the actor selects `hold`; X stays paused, with a persisted decision outcome and no new run. A forced fallback despite hold fails.
3. **S4-REJECT.** Given stale catalog, invalid model/protocol, missing provider credentials or changed workspace/schedule authorization, no update occurs, rejection is attributable, and an already running session stays unchanged.
4. **S4-RECOVERY.** If a permitted new model later fails at provider invocation, the run exposes failure and the decision owner sees a failure receipt; no automatic infinite retry or silent substitute.
5. **S4-COMPATIBILITY.** Schedules without the opt-in actor follow current CLI/API create/update/run behavior; ordinary team S2/S3/S3* mechanisms are unaffected.
6. **S4-COST.** Matched operator task manual update versus proposed composable path; implementation + integration + test + operator + maintenance minutes and task outcomes are recorded. `NOT_MEASURED` until measured.

**Stop/falsification:** no first-party developer actor or authority bridge; only a post hoc dashboard; existing native solution is sufficient; external model-change signal unreliable; no lawful option; no comparable operator result. Result remains **NEEDS_EVIDENCE** and there is **no implementation, test pass, regrade or cost saving**.

## Publication, legal and owner control

Apache-2.0 original, [contribution process](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/CONTRIBUTING.md) requires approved original issue before functional PR. This is fork metadata plan-only, not an external maintainer message. Human [issue.md](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/issue.md) remains the only public fork Issue candidate, subject to exact approval; this AI document is its linked technical companion. The fork's initial `DORMANT/PAUSE` is not an ALLOW/RESUME grant; no feature implementation/external issue/PR is authorized.
