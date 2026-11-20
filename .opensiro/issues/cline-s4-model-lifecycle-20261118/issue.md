# Cline — Wave 4 proposed S4 model-transition intelligence (Human roadmap)

**Target transition:** S4=— -> S4=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

**PLAN_ONLY · HYPOTHETICAL · NOT IMPLEMENTED · DRAFT — NOT PUBLISHED**

A developer could optionally compose an autonomous agent that anticipates externally announced model/provider changes, chooses a bounded future-session adaptation, and receives feedback from the actual subsequent Cline operation. The user still decides permitted models and ultimate policy.

The canonical [roadmap.md](roadmap.md) owns pins, historical vector, six-function priorities and status. [constructor-sufficiency.md](constructor-sufficiency.md) records native Track A/B interfaces and falsifiable tests. Stable case cline-s4-model-lifecycle-20261118 in verified opensiro-contributions/cline at opensiro/meta.

## Accepted Index and whole-repository screen

**Historical accepted vector, NOT current-HEAD regrade:** S1=A · S2=C · S3=C · S3*=C · S4=— · S5=—. [Included pinned assessment](https://github.com/opensiro/vsm-harness-index/blob/41ce68817f37a49158dceddf5d384863d54b4ee0/assessments/cl/cline.md), blob 7dcc1f6f9e1087b867f2074549949d3dd26a9ced, review cfe9cadab99617d5013bf89f07b079d105057791, 2026-09-15, Profile 0.2.1/Skills 0.3.1. [Original HEAD](https://github.com/cline/cline/commit/20b042723a14412f6c1e84230b008708534d6e8c) pinned independently on 2026-11-20.

| Function / role | Historical Index state | Current source-based owner / closure | Candidate / priority |
| --- | --- | --- | --- |
| **S1 · Operations** | A | First-party coding model/tool agent acts and responds to tool results | NO_TARGET |
| **S2 · Coordination** | C | Optional team tasks/dependencies/mailbox attenuate shared-work interference | NO_TARGET |
| **S3 · Current management** | C | Optional coordinator assigns and regulates active teammate commitments | NO_TARGET; return path |
| **S3* · Independent audit** | C | Optional reviewer and reviewed/rejected outcome fragments gate finalization | NO_TARGET |
| **S4 · External future adaptation** | — | Catalog/status and user model selection; autonomous future decision+feedback not evidenced | P0: prospective C proposal |
| **S5 · Identity/policy** | — | User/developer retains ultimate model policy and approvals | NO_TARGET, parent |

Whole-repository scope: first-party SDK, CLI, VS Code, Desktop, Hub, catalog/configuration, teams, plugins, cron, tests and relevant original Issues/PRs. Adjacent CI/dogfood, external provider governance and parent human authority excluded from autonomous S5. No claim intentional omission without evidence. A missing C is neither a defect nor a maturity ranking; no obligation to add all functions.

## Selected capability and native comparison

**Scenario (HYPOTHETICAL):** provider announces a future retirement or capability change. An optional source-attributed S4 agent evaluates real catalog options, chooses *retain*, *migrate candidate* or *hold*, and proposes an allowlisted future-session model; S3/host accepts or rejects it under parent policy. After the subsequent session, the outcome returns to the S4 decision owner.

**Track A:** [Catalog status/deprecation](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/llms/src/catalog/catalog-live.ts), [read-only provider catalog](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/apps/vscode/src/sdk/model-catalog/catalog.ts), [explicit model selection store](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/apps/vscode/src/sdk/model-catalog/store.ts), Core [plugin hooks](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/docs/sdk/plugins.mdx) and [scheduled execution](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/docs/sdk/guides/scheduled-agents.mdx). Merged original PR #15667 refreshes models; open PRs #15670 and #15677 address config/discovery. These do not establish an autonomous prospective choice owner.

**Track B:** reuse those native components, but add the smallest typed *future model-transition proposal + parent authorization + next-session acknowledgement/feedback* bridge. A notification or direct silent model rewrite is insufficient.

| Necessary C link | Native available (A) | Missing constructor (B) |
| --- | --- | --- |
| External future evidence | Model status and live metadata | Dated/provenanced future notice, candidate and autonomous S4 option selection |
| Legitimate effect | User model selection and next-session SDK config | Parent-scoped typed proposal, allowlist/veto, approved future application |
| Return feedback | Session/model events and afterModel hooks | Actual selected model/outcome returned to future S4 decisions |

**P0:** complete optional S4→S3→S4 construction. **P1:** rights, scoped host bridge, recency, compatibility and native tests. **P2:** NONE. Native/manual selection remains best cheap alternative for one-off model changes; maintenance/product fit is the maintainers' decision.

## Historical comparison and falsifier

Earlier 2026-11-19 [stable case](https://github.com/opensiro-contributions/cline/commit/3437b3be25df2404b19cc699a52590a46bbc6e0f) produced NO_GO for a different narrow question: current Hub restart [Issue #15795](https://github.com/cline/cline/issues/15795). Under new v0.18.0 neutrality, a current bug fix is not equivalent to a prospective autonomous S4 construction. New decision independently [sealed before historical reading](https://github.com/opensiro/upstream/issues/58#issuecomment-7043170806). Both decisions have their own scope and history; neither is product adoption.

**Positive proposed tests — NOT_RUN:** two distinct legitimate future model strategy choices; authorized *next* session consumes the approved model; selected model and outcome return. **Negative — NOT_RUN:** stale notice, unsupported model, absent/revoked parent approval, no live cloud session mutation and native unchanged fallback. **Falsifier:** equivalent already-shipped autonomous S4 future-loop or lawful post-choice effect/return cannot be completed. Benefit and cost remain NOT_MEASURED.

## Rights and next action

Fork owner state ACTIVE/ALLOW permits internal .opensiro metadata only. [Original CONTRIBUTING](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/CONTRIBUTING.md) requires an approved feature request for product changes. No external third-party or public fork Issue/PR/comment, product implementation, Index grade change or parent-policy delegation authorized. Research NEEDS_EVIDENCE, original-native tests NOT_RUN. AI-assisted draft; independent tests and maintainer acceptance are future separate decisions.
