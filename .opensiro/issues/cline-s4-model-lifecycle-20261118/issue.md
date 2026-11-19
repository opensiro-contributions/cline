# cline/cline — Upstream #58 independent Human roadmap

**Target transition:** NO_QUALIFIED_C_TARGET
**Proposal-stage decision:** NO_GO
**Research disposition:** NO_USEFUL_CHANGE

Canonical [roadmap.md](roadmap.md) · AI/developer [constructor-sufficiency.md](constructor-sufficiency.md). PLAN_ONLY, NOT PUBLISHED.

The accepted [Index assessment](https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/cl/cline.md) is historical (2026-09-15, Profile 0.2.1 / Skills 0.3.1, blob 7dcc1f6f9e1087b867f2074549949d3dd26a9ced); independently reviewed original [HEAD](https://github.com/cline/cline/commit/20b042723a14412f6c1e84230b008708534d6e8c) is current source, not current Index grade.

| Function / role | Historical Index | Current owner and source | Priority / candidate |
| --- | --- | --- | --- |
| **S1 · Operations** | A | first-party autonomous operational tasks under native tool feedback | NO_TARGET / DEFER |
| **S2 · Coordination** | C | optional team task board/mailbox provides composable coordination | NO_TARGET / DEFER |
| **S3 · Current regulation** | C | optional team lead controls active teammates and commitments | NO_TARGET / DEFER |
| **S3* · Independent audit** | C | reviewed/rejected fragments gate team outcome finalization | NO_TARGET / DEFER |
| **S4 · Prospective environment** | — | provider catalog refresh is not a developer-composed future environment decision owner | NO_TARGET / DEFER |
| **S5 · Ultimate identity/policy** | — | operator, deployment and user retain ultimate constraints | NO_TARGET / DEFER |

## Operator decision

**Question:** Observed Hub→local→Hub upgrade inconsistency; an autonomous outside/future model-strategy owner does not repair that same current-state bug. **Track A:** First-party provider catalog refresh, cache TTL and operator-selected provider configuration; issue #15795 shows running Hub not restarted by upgrade, not future/environment adaptation demand; team already reviews outcomes. **Track B:** No additional native S4 C port justified. Correct the Hub upgrade restart and provider invalidation via existing architecture before proposing a model lifecycle control actor.. **Rationale:** A measured provider deprecation or capability-shift scenario proves native catalog refresh and legitimate manual switching cannot adapt future runs, while a new bounded autonomous S4 actor produces distinct permitted later-operation feedback. Only a scoped NO_GO, not a rejection of original product.

## Sources, next step and rights

Original code [apps/vscode/src/sdk/model-catalog/catalog.ts](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/apps/vscode/src/sdk/model-catalog/catalog.ts); [sdk/packages/core/src/extensions/tools/team/multi-agent.ts](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/sdk/packages/core/src/extensions/tools/team/multi-agent.ts); [docs/cli/agent-teams.mdx](https://github.com/cline/cline/blob/20b042723a14412f6c1e84230b008708534d6e8c/docs/cli/agent-teams.mdx). Issues/PRs [issues / 15795](https://github.com/cline/cline/issues/15795); [pull / 15796](https://github.com/cline/cline/pull/15796). P1: Reproduce and route native #15795 running-Hub restart correctness; check existing provider picker and catalog invalidation. Earlier Cline roadmap was NEEDS_EVIDENCE on hypothetical S4 model lifecycle; this narrower current-head independent rerun finds no qualified C for the observed Hub route.. Native tests NOT_RUN, cost NOT_MEASURED. Fork owner control ACTIVE/ALLOW does not authorize an original maintainer message or a public fork Issue; both remain NOT PUBLISHED. AI-assisted draft.
