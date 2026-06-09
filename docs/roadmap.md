# Roadmap

## Phase 0: Documentation And Product Definition

Goals:

- Define vision.
- Define MVP scope.
- Define workflows.
- Define domain model.
- Identify open product, legal, payment, and trust questions.

Deliverables:

- Initial docs.
- Product decision log.
- MVP build plan.

## Phase 1: Manual MVP

Goals:

- Let project owners create projects and tasks.
- Let contributors claim and submit tasks.
- Let reviewers approve, reject, or request changes.
- Track transparent value allocation in a ledger.

Deliverables:

- Auth and user profiles.
- Project dashboard.
- Task marketplace.
- Task claim and submission flow.
- Review flow.
- Ledger view.
- Basic reputation events.

## Phase 2: Trust And Quality

Goals:

- Improve review reliability.
- Reduce abandoned tasks.
- Add dispute handling.
- Make reputation useful for task matching.

Deliverables:

- Reviewer assignment rules.
- Claim expiration.
- Dispute workflow.
- Skill-specific reputation.
- Contributor reliability metrics.
- Review accuracy metrics.

## Phase 3: Assisted Coordination

Goals:

- Help project owners decompose work.
- Help contributors find suitable tasks.
- Help reviewers evaluate submissions consistently.
- Start formalizing contribution events beyond task completion.

Deliverables:

- AI-assisted task drafting.
- Task templates by project type.
- Suggested acceptance criteria.
- Contributor-task matching.
- Review checklist generation.

## Phase 3.5: Groups And Containers

Goals:

- Introduce persistent collaboration structures.
- Support earlier-stage ideas and recursive decomposition.
- Test governance without overbuilding organizational complexity.

Deliverables:

- Draft ideas.
- Project conversion from ideas.
- Basic groups.
- Group templates.
- Group-owned projects.
- Public pledges.
- Contribution event graph.
- Decomposition credit for coordinators.

## Phase 4: Marketplace Expansion

Goals:

- Increase liquidity.
- Support broader project types.
- Improve payment automation.

Deliverables:

- Public project discovery.
- Contributor search.
- Saved skills and interests.
- Payment provider integration.
- Payout status tracking.
- More artifact types.

## Phase 5: Decentralized Governance Experiments

Goals:

- Test community-led validation and coordination.
- Let high-reputation users help govern work quality.

Deliverables:

- Multi-reviewer workflows.
- Community arbitration.
- Reputation-weighted review experiments.
- Transparent fee and reserve reporting.

## Phase 6: Residual Value Experiments

Goals:

- Test whether upstream contribution rights can be represented fairly.
- Compensate useful ideation, research, and decomposition when downstream work creates value.
- Explore non-withholding legal wrappers for patents, businesses, and licenses.

Deliverables:

- Residual claim model.
- Contribution weight experiments.
- Downstream dilution rules.
- Legacy idea policy.
- Claim dispute workflow.
- Legal wrapper policy draft.
- Spinout and fork value-routing rules.

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

Deliverables:

- Research input model.
- Veracity scoring prototype.
- Public problem bounty prototype.
- Safety and liability requirements.
- Real-world task feasibility review.

## Phase 9: Protheus/InfRing Network Transition

Goals:

- Evaluate Storm running on Protheus network primitives once InfRing v2 supports network-node operation.
- Replace platform authority with receipt-backed, locally validated network trust where practical.

Deliverables:

- Minimal Storm receipt format.
- Node identity mapping.
- Project-state receipt export.
- Ledger-event receipt export.
- Contribution-event receipt export.
- Local validation rules for incoming network signals.
- Federated task/project discovery prototype.

## Roadmap Guardrail

Do not expand into broad marketplace discovery before the core loop works:

Project -> Task -> Claim -> Submit -> Review -> Ledger -> Reputation.
