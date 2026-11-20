# Cline — Wave 4 S4 model-transition constructor technical contract

**Target transition:** S4=— -> S4=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

**Source of truth:** [roadmap.md](roadmap.md) — canonical accepted historical vector and all six dispositions; do not reinterpret those grades here. Human [issue.md](issue.md) contains the single combined six-function table. This is PLAN_ONLY, NOT_IMPLEMENTED, NATIVE_TESTS_NOT_RUN and NOT_PUBLISHED.

## Boundary and function-specific right

Original pinned cline/cline main [20b042723a14412f6c1e84230b008708534d6e8c](https://github.com/cline/cline/commit/20b042723a14412f6c1e84230b008708534d6e8c). First-party model/provider/catalog, SDK startup and session feedback in llms/agents/core with CLI/VS Code/Desktop and supported Hub mode; optional plugins and scheduled runs. The requested S4 owner is an OPTIONAL developer-composed autonomous investigator with discretion to choose among future model transition options based on external *prospective* evidence. It is **not** the vendor's governance process, a maintainer PR workflow, routine bugfix, simple status filter, current token budget, or a general S5 policymaker. S1 operational agent acts; S2 peer coordination and S3 commitments remain; S3* independent reviewer is untouched; S4 offers future options to real S3; user/parent retains S5 ultimate permission.

**Counterfactual owner test:** remove proposed S4 agent, leave cron, catalog, model picker and Core sessions. User can still manually change models and provider status still filters, but no autonomous source-attributed future strategy choice/closed feedback exists. Remove only alert transport: S4 reasoning could still make a choice but without approved S3 effect it cannot close S4. Proposed S4 is decisive for the prospective *choice*, NOT for ultimate selection permission.

## Track A: actual first-party and original overlap

- [SDK layering](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/ARCHITECTURE.md): model/provider concerns in llms, run hooks/tools in agents, persistence/session/cron in core. Existing packages/README states the same architectural authority boundary.
- [catalog-live.ts](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/llms/src/catalog/catalog-live.ts): reads provider model metadata including status and release date, filters deprecated builtins. No autonomous future-options selection evidenced.
- [catalog.ts](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/apps/vscode/src/sdk/model-catalog/catalog.ts): read-only reader cannot call write/commitSelection and refreshes provider model snapshots.
- [store.ts](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/apps/vscode/src/sdk/model-catalog/store.ts): explicit commitSelection writes chosen provider model; provider config patch cannot write model selection.
- [Plugins](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/docs/sdk/plugins.mdx) can compose beforeModel, afterModel and runtime events. [Scheduled agents](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/docs/sdk/guides/scheduled-agents.mdx) and core cron can trigger optional research; generic hook or schedule is NOT automatically S4 C.
- [Cloud-session host](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/apps/vscode/src/sdk/cloud-session-host.ts) deliberately does not support updating running session model; no proposed path may assume it.
- Original [PR #15667](https://github.com/cline/cline/pull/15667) MERGED credential model refresh; [PR #15670](https://github.com/cline/cline/pull/15670) OPEN migration of provider setting selection; [PR #15677](https://github.com/cline/cline/pull/15677) OPEN discovered context metadata. None establishes complete S4 prospective independent owner. Existing [Issue #15795](https://github.com/cline/cline/issues/15795) OPEN current Hub restart incident is a different operator problem. Previously cited [PR #15796](https://github.com/cline/cline/pull/15796) is an unrelated OPEN docs package-name PR, not #15795 remediation.

## Track B: necessary smallest function-specific construction

Three conceptual alternatives were screened: (1) warn/refresh/parent switch — no autonomous S4 owner; (2) scheduled digest — future alert but no S3 decision application and returned feedback; (3) **selected**, optional new C constructor combining existing native loop/cron/catalog/config with **one minimum typed future-session model-transition proposal/acknowledgement path**.

| Native integration | Existing original source | Minimal additional construction | Owner, effect, return |
| --- | --- | --- | --- |
| Prospective signal and evaluation | llms catalog model status/release_date; core cron and agent/plugin runtime | Optional source provenance/recency ingestion; S4 agent exposes distinct retain/migrate/hold options from available next-session model capabilities | S4 agent legitimately chooses future plan, not vendor or deterministic status filter |
| Future model proposal | SDK config providerId/modelId and parent-controlled store | Typed proposal with source evidence, target future session, candidate, expiry, allowed modes, observed rationale | S4 proposes; Core/host rejects unsupported model or stale proposal; user/policy may veto |
| Authorized session effect | Core starts sessions with host configuration; existing user config/selection | Host adapter validates parent allowlist/explicit approval; applies only to new next-session config, not running cloud session; acknowledgement records accept/reject and chosen model | Legitimate S3/host executes, not untrusted plugin bypassing policy |
| Feedback loop | Existing run lifecycle and afterModel, session model and result events | Durable correlated acknowledgement and returned actual selected provider/model, run result or failure to optional S4 owner | S4 observes outcome, revises later prospective model choice |

**Architectural sufficiency:** The combined existing and proposed native mechanism creates a separately composed prospective decision owner, a legitimate *alternative model choice*, a real first-party new session effect after parent permission and a feedback path closing future S4 interpretation against current S3. All four obligations are required together. Hooks alone can observe but do not guarantee authority or closure; host port is therefore newly proposed, not claimed already shipped. Scope must be experimentally verified across SDK/CLI/VS Code/Hub, with parent rights and cloud restrictions. Future model choice and permission are separate; no authority to modify ultimate policy, credentials or running agents.

**Necessary dependency order:** P1 evidence input contract and model compatibility → P1 scoped model-transition host adapter and parent gate → P0 optional S4 actor + new-session acceptance + feedback tests. P2 NONE. The native manual alternative is retained and preferable if experiments show no additional constructibility benefit or maintenance burden unjustified. The research does not decide maintainer product preference.

## Future source-native acceptance — all NOT_RUN

Native sources contain [llms catalog tests](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/llms/src/catalog/catalog-live.test.ts), [VS Code catalog/store tests](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/apps/vscode/src/sdk/model-catalog/store.test.ts), core/cron tests and plugin examples; no new tests executed. Under Cline CONTRIBUTING, use the original Bun/Vitest/test scripts and selected package fixtures when separately implementing. The following are **proposed test cases, not passing assertions**.

| Proposed native case | Setup and expected observable effect | Falsifier |
| --- | --- | --- |
| Prospective choice | Two independently sourced dated future provider notices produce distinguishable valid retain/migrate/hold decisions from composed S4 actor | Output is fixed template or solely status filtering |
| Authorized future action | Valid model candidate and parent allowlist permit next-session SDK config to use chosen model; correlation confirms the actual run model and result return to S4 | Only advisory output, host ignores it, no returned run result |
| Parent veto | No permission/revoked approval/restricted model leaves existing config intact and returns explicit rejection | S4 bypasses policy or silently replaces model |
| Stale/invalid evidence | Expired provider notice or candidate absent from catalog is rejected or held with reason, no forced transition | Unsupported selection applies anyway |
| Cloud and baseline | Existing manual model selection preserved; running cloud session not modified, optional S4 off restores baseline | Unexpected live mutation or changed no-agent behavior |

**Primary falsifier:** an actually shipped equivalent autonomous prospective S4 loop, or infeasibility of legitimate host next-session application and correlated return. A manual fix of current Hub bug #15795 is not an equivalent function-owner chain. Demand, cost, benefit and native test outcome **NOT_MEASURED / NOT_RUN**.

## Decision, history and rights

**GO + NEEDS_EVIDENCE** is a structurally coherent proposed C-constructor hypothesis without executed validation, not shipped C or Index reclassification. Independent v0.18.0 first pass [sealed here](https://github.com/opensiro/upstream/issues/58#issuecomment-7043170806) before old case read. Earlier [2026-11-19 scoped NO_GO case](https://github.com/opensiro-contributions/cline/commit/3437b3be25df2404b19cc699a52590a46bbc6e0f) was focused on the present Hub restart bug; preserve original event/history and distinguish new S4 future object. No external original/fork-public Issue/PR/comment, product implementation or grade change authorized. [Human issue.md](issue.md); [canonical roadmap.md](roadmap.md). AI-assisted research, full source-native tests still required.
