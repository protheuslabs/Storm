# Roadmap

## Phase 0: Documentation And Product Definition

Goals:

- Define vision.
- Define MVP scope.
- Define workflows.
- Define domain model.
- Define public positioning and first wedge.
- Define subsystem boundaries.
- Define subsystem inventory and first-build priorities.
- Identify open product, legal, payment, and trust questions.

Current Tentative Definition Package:

1. Core thesis and position
- Keep the thesis narrow enough to execute: Story Forge is the first public wedge.
- Keep the broader thesis explicit but internal: Storm is the coordination/value-routing substrate.
- Document what is in-scope for proof versus future ecosystem ambition.

2. Core platform contract
- Fix the non-negotiable primitive set: Projects, Tasks, Claims, Submissions, Reviews, Disputes, Reputation, Ledger, Contribution Events, Provenance.
- Define state transitions, validation rules, and what counts as authoritative truth at each transition.
- Define the minimum set of terms everyone can point to before engineering starts.

3. Governance contract
- Clarify Protheus stewardship, visible origin claim, and stewardship decay rules.
- Define release-switch trigger conditions and what powers are removed when each threshold is crossed.
- Define anti-capture requirements: transparency, appealability, provenance, agent disclosure, and explicit bounded controls.

4. Economics contract
- Lock task payout behavior for MVP (fixed visible task values).
- Define dispute and correction behavior before variable contribution weighting.
- Define where residual and upstream value could exist later without destabilizing the first loop.
- Define value ledger visibility and minimum explanation requirements.

5. Applet contract
- Define what remains in Storm core versus what stays applet-specific.
- Define the first applet boundary (Story Forge) and the domain-semantics interface.
- Define applet onboarding pattern so the next applet (Code Forge etc.) can be introduced safely.

6. Integration and network contract
- Define which native mechanisms are scaffolding versus durable primitives.
- Define how decomposition, receipts, provenance, and rights evidence map to InfRing when ready.
- Define what data is shared across products and what remains local.
- Define initial bot/agent trust boundaries without adding full automation.

Deliverables:

- Initial docs.
- Product decision log.
- Storm definition gate checklist.
- MVP build plan.
- Positioning and first-wedge doc.
- Subsystem modularity plan.
- Subsystem inventory.

Readiness Gate:

- Phase 1 starts only when the definition package has clear owners, stable terms, and an explicit list of unresolved questions.
- If unresolved questions are mostly implementation details, continue in Phase 0.
- If unresolved questions are core thesis or contract questions, delay implementation until they are resolved.
- If any required checklist item is not `Ready`, maintain Phase 0 and do not ship implementation scope.

## Phase 0 Readiness Artifact

- Current readiness artifact: [Storm Definition Gate](docs/storm-definition-gate.md).

## Phase 1: Manual MVP

Goals:

- Let project owners create projects and tasks.
- Let contributors claim and submit tasks.
- Let reviewers approve, reject, or request changes.
- Track transparent value allocation in a ledger.
- Use fixed visible task values rather than algorithmic contribution scoring.
- Prove Story Forge as the first public crowdsourced project vertical.
- Keep MVP code modular enough for later subsystem expansion.
- Establish workflow orchestration, artifact storage, and audit/event foundations.

Deliverables:

- Auth and user profiles.
- Project dashboard.
- Task marketplace.
- Story project fields and story task templates.
- Story Forge public project loop.
- Task claim and submission flow.
- Review flow.
- Ledger view.
- Default fixed-task-value policy.
- Basic reputation events.
- Initial subsystem interfaces and contract tests.
- Basic artifact records.
- Structured workflow/audit events.

## Phase 2: Trust And Quality

Goals:

- Improve review reliability.
- Reduce abandoned tasks.
- Add dispute handling.
- Make reputation useful for task matching.
- Start making value explanations consistent across tasks, reviews, fees, and adjustments.
- Start separating reputation from fraud and risk signals.
- Start defining allowed execution modes for human, assisted, and automated work.

Deliverables:

- Reviewer assignment rules.
- Claim expiration.
- Dispute workflow.
- Skill-specific reputation.
- Contributor reliability metrics.
- Review accuracy metrics.
- Allocation explanation template.
- Initial fraud/risk signal inventory.
- Basic AI-assistance disclosure field.

## Phase 3: Assisted Coordination

Goals:

- Help project owners decompose work.
- Help contributors find suitable tasks.
- Help reviewers evaluate submissions consistently.
- Start formalizing contribution events beyond task completion.
- Formalize applet task templates and review rubrics.
- Prepare value policy records for applet-specific contribution types.

Deliverables:

- AI-assisted task drafting.
- Task templates by project type.
- Suggested acceptance criteria.
- Contributor-task matching.
- Review checklist generation.
- Applet-aware value policy draft.

## Phase 3.25: Applet Framework

Goals:

- Generalize the Story Forge vertical into a reusable applet pattern.
- Keep Storm core generic while supporting domain-specific project workflows.

Deliverables:

- Applet contract.
- Applet project templates.
- Applet task templates.
- Applet review rubrics.
- Applet artifact type registry.
- Code Forge feasibility sketch.
- Invention Forge feasibility sketch.

## Phase 3.5: InfRing Task Decomposition Integration

Goals:

- Use InfRing task decomposition primitives to generate project task candidates.
- Preserve applet-specific constraints while relying on InfRing for receipted decomposition.

Deliverables:

- Storm-to-InfRing decomposition request contract.
- InfRing task candidate import format.
- Story Forge decomposition constraints.
- Task candidate review and acceptance workflow.
- Provenance mapping from InfRing task output to Storm task records.

## Phase 3.75: Groups And Containers

Goals:

- Introduce persistent collaboration structures.
- Support earlier-stage ideas and recursive decomposition.
- Test governance without overbuilding organizational complexity.
- Preserve project lineage as ideas, groups, and projects branch or evolve.

Deliverables:

- Draft ideas.
- Project conversion from ideas.
- Basic groups.
- Group templates.
- Group-owned projects.
- Public pledges.
- Contribution event graph.
- Decomposition credit for coordinators.
- Simple parent-project lineage for forks or spinouts.

## Phase 4: Marketplace Expansion

Goals:

- Increase liquidity.
- Support broader project types.
- Improve payment automation.
- Introduce search, discovery, and matching as a real subsystem.

Deliverables:

- Public project discovery.
- Contributor search.
- Task search and ranking.
- Skill and interest indexing.
- Saved skills and interests.
- Payment provider integration.
- Payout status tracking.
- More artifact types.

## Phase 5: Decentralized Governance Experiments

Goals:

- Test community-led validation and coordination.
- Let high-reputation users help govern work quality.
- Improve fraud, risk, and anti-collusion controls.
- Introduce bot-control and authorized-agent participation rules.

Deliverables:

- Multi-reviewer workflows.
- Community arbitration.
- Reputation-weighted review experiments.
- Transparent fee and reserve reporting.
- Review-ring and collusion detection prototype.
- Authorized-agent policy draft.
- Unauthorized bot-use risk signals.

## Phase 5.5: Originality And Rights Enforcement

Goals:

- Prevent copied or rights-incompatible work from contaminating Storm projects.
- Protect Storm contributors from plagiarism by other users.
- Reduce risk from importing legally owned external material without permission.
- Use AI-assisted similarity and rights analysis as evidence, not final judgment.

Deliverables:

- Contributor originality and permission attestations.
- Internal Storm source corpus.
- Submission originality check pipeline.
- Similarity match records.
- Rights policy metadata.
- Rights review workflow.
- Quarantine and payout-hold states.
- Appeal and dispute path for false positives.
- Applet-specific risk checks for Story Forge, Code Forge, and Invention Forge.

## Phase 6: Residual Value Experiments

Goals:

- Test whether upstream contribution rights can be represented fairly.
- Compensate useful ideation, research, and decomposition when downstream work creates value.
- Explore non-withholding legal wrappers for patents, businesses, and licenses.
- Introduce contribution valuation experiments with visible policy versions.
- Preserve value routing through forks, spinouts, and merged project lines.

Deliverables:

- Residual claim model.
- Contribution weight experiments.
- Contribution valuation model.
- Allocation explanation records.
- Downstream dilution rules.
- Legacy idea policy.
- Claim dispute workflow.
- Legal wrapper policy draft.
- Spinout and fork value-routing rules.
- Fork lineage and merge-proposal experiment.

## Phase 7: AI Training Provenance

Goals:

- Allow approved AI training on Storm and Protheus Labs ecosystem data without erasing contributor provenance.
- Route value back to source contributors when AI-generated value can be attributed.

Deliverables:

- Dataset version model.
- Dataset source manifest.
- Training-run records.
- AI value event records.
- Attribution methods.
- Dataset pool allocation experiments.
- AI attribution dispute workflow.

## Phase 8: Intelligence And Real-World Bounty Research

Goals:

- Explore World Eye-style problem intelligence.
- Explore Bolt-style real-world bounties only after legal and safety analysis.
- Define privacy, consent, and data-access boundaries for broader data use.

Deliverables:

- Research input model.
- Veracity scoring prototype.
- Public problem bounty prototype.
- Safety and liability requirements.
- Real-world task feasibility review.
- Privacy and consent review.

## Phase 9: Protheus/InfRing Network Transition

Goals:

- Evaluate Storm running on Protheus network primitives once InfRing v2 supports network-node operation.
- Replace platform authority with receipt-backed, locally validated network trust where practical.
- Start phasing out Storm-native mechanisms when mature InfRing primitives can safely replace them.
- Evaluate an InfRing versioning/fork subsystem for project lineage, merge, and fork mechanics.

Deliverables:

- Native mechanism inventory.
- Primitive replacement criteria.
- Adapter and interface audit.
- Subsystem boundary audit.
- Minimal Storm receipt format.
- Node identity mapping.
- Project-state receipt export.
- Ledger-event receipt export.
- Contribution-event receipt export.
- Value-policy execution migration plan.
- Provenance and dataset lineage migration plan.
- Version/fork lineage migration plan.
- Native mechanism deprecation plan.
- Local validation rules for incoming network signals.
- Federated task/project discovery prototype.

## Phase 10: Release Switch

Goals:

- Transition Storm from Protheus Labs-operated platform to network-governed system when critical mass and trust requirements are met.
- Preserve transparent Protheus Labs origin value without preserving unilateral control.

Deliverables:

- Release criteria.
- Governance handoff plan.
- Protocol origin allocation model.
- Hidden-control audit.
- Network governance policy.
- Emergency authority policy.
- Release-switch rehearsal.
- Public release-switch report.

## Roadmap Guardrail

Do not expand into broad marketplace discovery before the core loop works:

Project -> Task -> Claim -> Submit -> Review -> Ledger -> Reputation.
