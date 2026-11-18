# Cline — source-native S4 model-lifecycle adaptation roadmap (OpenSiro plan-only)

**OpenSiro pilot · PLAN_ONLY / NEEDS_EVIDENCE · DRAFT — NOT PUBLISHED**  
**Working fork:** https://github.com/opensiro-contributions/cline · **case:** `.opensiro/issues/cline-s4-model-lifecycle-20261118/` on `opensiro/meta`  
**AI/developer contract:** [constructor-sufficiency.md](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/constructor-sufficiency.md) · **technical receipt:** [roadmap.md](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/roadmap.md)

## 1. Why OpenSiro and the accepted VSM assessment

OpenSiro tests whether VSM-informed reusable organizational specifications and source-native integrations can **standardize AI-agent harness development and reduce engineering/integration/maintenance cost**. This is an unmeasured hypothesis, not a claim of demonstrated savings or a request for maintainers to adopt VSM.

> **ACCEPTED HISTORICAL INDEX — NOT CURRENT HEAD AND NOT A TARGET:**  
> **S1=A · S2=C · S3=C · S3*=C · S4=— · S5=—**  
> [Accepted assessment](https://github.com/opensiro/vsm-harness-index/blob/5f6ea0c777733813ca42e3f210390a719488dcfb/assessments/cl/cline.md); assessment blob `7dcc1f6f9e1087b867f2074549949d3dd26a9ced`; `review_ref=cfe9cadab99617d5013bf89f07b079d105057791`; reviewed `2026-09-15`, checked `2026-09-17`; Profile `0.2.1` / Skills `0.3.1`.

| Function | Accepted ownership state | Consequence for this roadmap |
| --- | --- | --- |
| S1 · Coding operations | **A** | Preserve agent coding capability; no required C conversion |
| S2 · Team coordination | **C** | Optional team mailbox/task board; not a reason to build another coordinator |
| S3 · Team current control | **C** | Optional team lead/commitment control; preserve local schedule rights |
| S3* · Complementary review | **C** | Composable team review/finalization; no forced auditor |
| S4 · External/future adaptation | **—** | Historical non-establishment; inspect **current** catalog and scheduler before proposing an S4 constructor |
| S5 · Ultimate policy | **—** | Do not infer new delegated identity/policy authority; operator remains the protected decision owner |

**Source and boundary.** Current original `cline/cline@eff43e19b267e171f597ab03733bfed25090f72d` observed 2026-11-18; the [source commit](https://github.com/cline/cline/commit/eff43e19b267e171f597ab03733bfed25090f72d) is much newer than the accepted Index review. Target only the **first-party SDK/CLI hub scheduled-agent mode plus its shared model catalog**, with scheduled runs as operational units/episodes. Do not transfer the Index's team-mode C grades automatically to a different supported mode; the complete vector above is historical repository-relative evidence. Exclude Cline maintainers, remote model providers, private Cloud services and uninstalled plugins from the assessed runtime. The last accepted semantic check is 62 days old: recommend a separate Index-owned pinned reassessment before relying on historical grades, but this is not a roadmap blocker.

**Rights.** Original [Apache-2.0](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/LICENSE). The [contributor guide](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/CONTRIBUTING.md) requires an issue/approved feature proposal before implementation, and says PR contributions use the project's license. This fork-only plan is not an original-repository issue, implementation, PR or maintainer approval. Fork metadata is initialized restrictively (`DORMANT/PAUSE`); no further engineering is granted.

## 2. Candidate user capability and decision

**P0 candidate — developer-composable S4 model-lifecycle adaptation for future scheduled runs.** A Cline SDK developer with several scheduled coding/maintenance agents wants to respond when an external provider deprecates a model or changes its supported capabilities. They should be able to supply their *own* decision actor to compare real options (`retain`, `hold`, or eligible replacement), submit a scoped authorized change for **future** schedule execution, and inspect actual next-run feedback. A model-catalog refresh or forced fallback alone is not S4 ownership.

**What remains unproven:** no retrieved original Issue explicitly requests this end-to-end scheduled-agent capability, and current first-party availability of a suitably scoped developer decision-port-to-schedule bridge is unverified. Do **not** implement a new controller merely to fill historical `S4=—`. First validate a concrete user/task counterfactual and the existing plugin/API alternative. **Decision: NEEDS_EVIDENCE, not implementation-ready.**

**Cheapest native alternative:** a human checks provider metadata, changes the selected model by [supported schedule updates](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/core/src/cron/service/schedule-tool.ts) / CLI settings, and observes later [schedule runs](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/docs/sdk/guides/scheduled-agents.mdx). If that resolves the demonstrated need with lower cost, stop at `NO_USEFUL_CHANGE`.

## 3. Shipped work versus missing capability

| Topic | Evidence at pinned original HEAD and original tracker | Residual to verify |
| --- | --- | --- |
| External model facts | [ModelInfo](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/shared/src/llms/model-info.ts) has status, deprecation, replacement, pricing and capability fields; [catalog refresh config](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/llms/src/providers/config.ts) and [recommended models](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/llms/src/catalog/catalog-cline-recommended.ts) already exist | Are external changes compared and converted into future options *for a particular running schedule*? |
| Native schedule action | [Schedule tool](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/core/src/cron/service/schedule-tool.ts) includes `update`/`pause`/`resume` and `model_selection`; [CLI selection](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/apps/cli/src/commands/schedule/model-selection.ts) chooses explicit or saved model; [schedule service](https://github.com/cline/cline/blob/eff43e19b267e171f597ab03733bfed25090f72d/sdk/packages/core/src/cron/service/schedule-service.ts) stores model selection and run status | Is a narrowly scoped autonomous developer decision actor authorized to apply the choice to later runs and see the result without hijacking active execution? |
| Real external variability | Original [#15446](https://github.com/cline/cline/issues/15446) (model variant context metadata), [#15481](https://github.com/cline/cline/issues/15481) (displayed vs actual provider pricing), [#13921](https://github.com/cline/cline/issues/13921) (API protocol incompatibility) were **OPEN** on 2026-11-18 | These are problem evidence, **not** endorsements or already-implemented S4 roadmap work |
| Related original PRs | [#12357](https://github.com/cline/cline/pull/12357) Bedrock base-model capabilities **OPEN**; [#15670](https://github.com/cline/cline/pull/15670) provider-settings refactor **OPEN**; [#15499](https://github.com/cline/cline/pull/15499) token budget fix **MERGED** | Respect pending/merged behavior; none was confirmed to implement the complete proposal |

## 4. Priority and minimum sufficient result

| Priority | User outcome | Minimum verified construction |
| --- | --- | --- |
| **P0 · S4** | Developer's eligible adaptation decision actually affects a subsequent scheduled run and returns feedback | external dated distinction → versioned alternatives → **developer-composed decision actor** → scoped authorized schedule update/hold → subsequent run/model/status receipt, including S3 resource impact |
| **P1 · before P0** | Demonstrate necessity and protect native behavior | verify operator demand, existing SDK/plugin composition, catalog provenance, schedule ownership/permissions, no changes to active run, negative tests and reproducible first-party mode |
| **P2 · NONE** | No independently demonstrated second capability | Do not force S3/S5 changes or an imaginary `C → C(P) → A(P)` ladder |

**Sufficiency:** the [AI contract](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/constructor-sufficiency.md) specifies five conditional ports and source-native test ideas; they are a proposed design, **not existing shipped interfaces**. The current verdict is `NEEDS_EVIDENCE` until a real operator need and authorized supported integration are demonstrated.

## 5. Acceptance and stop criteria

| Proposed check (NOT executed) | Positive observable effect | Stop / fail-closed |
| --- | --- | --- |
| Model withdrawn before next recurring run | Developer actor considers ≥2 valid options, approves one, next *new* run uses chosen model, returned run receipt records model and outcome | A notice, manual suggestion, or provider hardcoded fallback is all that exists |
| Alternative lawful choice | With the same catalog change, actor chooses `hold` instead of replacement; schedule stays paused and no next run starts | Core silently overrides the choice |
| Invalid or unauthorized change | Changed/revoked schedule owner, stale metadata, unsupported provider or lacking credentials leaves configuration unchanged with denial reason | Tool applies cross-workspace/unsupported model anyway |
| Baseline/control comparison | Same workload and rights versus current manual scheduler update; measurable material improvement, no regression to normal schedule execution | New ports duplicate the existing native/plugin path without value |

Do not claim executed tests or Index grade changes from a design. Preserve human-owned policy boundaries and any existing S3/S3* reviewer decisions.

## 6. Independent paths

(a) Original-native manual/small-feature path first, with approved issue required before implementation; (b) optional Profile/Skills feedback only for independently evidenced semantic ambiguity; (c) optional legally permitted domain experiment with its own scope. No direct posting or product changes in this pilot.

## 7. Cost hypothesis

Compare **the same scheduled-agent adaptation task** under manual Cline configuration and a composable S4 port: actual next-run success/quality, operator minutes, implementation/integration/review/test effort, failures, and maintenance/regression cost. **Cost status: NOT_MEASURED**. A generic design pattern is not proof of cost reduction.

## 8. Decision and handoff

**NEEDS_EVIDENCE / PLAN_ONLY.** First confirm original-native scheduled-workload demand and whether the current SDK/plugin composition can already realize authorized selection and feedback. If native functionality suffices, close `NO_USEFUL_CHANGE`. Otherwise a separately approved full-cycle `upstream upgrade cline/cline` can implement/test the smallest first-party path. Full [AI contract](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/constructor-sufficiency.md) and [receipt](https://github.com/opensiro-contributions/cline/blob/opensiro/meta/.opensiro/issues/cline-s4-model-lifecycle-20261118/roadmap.md) remain on the verified fork.

**Public Issue:** fork-local only, NOT PUBLISHED until exact current-conversation approval of this title/body. **Original repository:** no issue, comment or PR. **AI disclosure:** AI-assisted plan; no independent human validation, native tests or cost savings claimed.
