# Cline — Upstream #58 Wave 4, native-specific v0.18.1 continuation

**2026-11-20 · SAME RUN, NOT A NEW INDEPENDENT RE-RUN** · original [cline/cline@20b042723](https://github.com/cline/cline/commit/20b042723a14412f6c1e84230b008708534d6e8c).

**Proposal-stage GO / research NEEDS_EVIDENCE · S4=— -> S4=C (HYPOTHETICAL, NOT SHIPPED)**. Accepted historical Index S1=A · S2=C · S3=C · S3*=C · S4=— · S5=— unchanged.

[Canonical roadmap receipt](roadmap.md) · [Human issue draft](issue.md) · [AI source-native constructor](constructor-sufficiency.md).

## Specific Cline construction

Prior generic proposed "model transition Host port" was narrowed under [integrated v0.18.1 native-specific advisory](https://github.com/opensiro/upstream/blob/main/changes/v0.18.1.md):

- Scope is one **Cline Core Hub recurring schedule** and its selected model, not a global session/provider mutation.
- An optional autonomous S4 researcher compares externally dated provider/model future notices, selects retain/migrate/hold, and explains the recommendation for that schedule.
- Existing first-party `tasks.scheduled` **update** already supports `model_selection` but explicitly **requires an interactive user session** and matching workspace. Do **not** use a headless scheduled agent to mutate schedules.
- After parent-authorized interactive update, `HubScheduleService` persists the selection, `CronRunner.buildStartRequest` uses it on a future run, and Core execution events/history can supply outcome. The research gap is reliable *proposal → authorized schedule revision → actual next-run model/outcome* correlation for the S4 investigator, not a general-purpose new Host write API.
- Native behavior tests **NOT_RUN**, technical benefit/cost **NOT_MEASURED**. No original code or Index changes, no maintainer approval or additional authority presumed.

## Provenance and rights

The [v0.18.0 first-pass decision](https://github.com/opensiro/upstream/issues/58#issuecomment-7043170806) was sealed independently; [prior v0.18.0 Cline metadata commit](https://github.com/opensiro-contributions/cline/commit/e6a12a8fba0bfe7399c5e00cfc3f818f05e6940b) remains in Git history. An even older [2026-11-19 NO_GO](https://github.com/opensiro-contributions/cline/commit/3437b3be25df2404b19cc699a52590a46bbc6e0f) addressed the *current-state Hub upgrade issue*, not this prospective future-option constructor. No result overwritten without provenance; this is same-case refinement.

Owner `ACTIVE/ALLOW` covers internal `opensiro/meta` research only. External/public fork GitHub Issue, original PR/comment/issue **NOT_PUBLISHED**, no product implementation, no test execution.

Under [Upstream reporting hygiene](https://github.com/opensiro/upstream/blob/main/docs/ROADMAP_INDEPENDENT_RERUN.md) there is **no new per-run upstream .md or PR**. Historical [PR #84](https://github.com/opensiro/upstream/pull/84) is already closed unmerged and linked in the one [Supplementary report](https://github.com/opensiro/upstream/blob/main/docs/ROADMAP_REPORT.md#supplementary); active completion belongs in existing [Upstream #58](https://github.com/opensiro/upstream/issues/58).

**Validation:** Current Upstream `scripts/validate_capability_roadmap.py <case-dir>` is the structural check to run after writing this case. Any such PASS validates formatting only, not S4 semantic closure or native tests.
