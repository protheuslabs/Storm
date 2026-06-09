# Decision Log

This file records product and technical decisions as the project evolves.

## Format

Each decision should include:

- Date.
- Decision.
- Context.
- Alternatives considered.
- Consequences.

## Decisions

### 2026-06-09: Start With Documentation First

Decision:

Storm will begin with product and architecture documentation before application scaffolding.

Context:

The project combines marketplace mechanics, project management, review, reputation, and payments. These areas have high product risk and need clear assumptions before implementation.

Alternatives considered:

- Scaffold the app immediately.
- Start with brand and landing page design.
- Start with payment or marketplace infrastructure.

Consequences:

- Early work focuses on defining the core loop and incentive model.
- Engineering implementation can follow a clearer MVP scope.
- Some technical choices remain intentionally open.

### 2026-06-09: Manual MVP Before Automation

Decision:

The first MVP should support manually created tasks and manually performed review before relying on AI automation.

Context:

Storm's long-term vision includes automated and crowdsourced coordination, but task decomposition and review incentives need validation first.

Alternatives considered:

- Build AI task decomposition as the first core feature.
- Build a broad marketplace with minimal workflow structure.

Consequences:

- The first product can test trust, review, and payout mechanics directly.
- AI assistance can be added later on top of observed workflows.
- The MVP remains smaller and easier to verify.

### 2026-06-09: Preserve Old Vision As Layered Scope

Decision:

Concepts from the old Storm document will be captured in docs, but split into MVP, platform, expansion, and research layers.

Context:

The old document includes residual compensation, idea containers, groups, alliances, World Eye, Bolt, IP protection, robotics, fabrication, and institution-scale goals. These are important to the vision but too broad for the first product build.

Alternatives considered:

- Treat the old document as the full MVP spec.
- Ignore the old document and keep only the new marketplace framing.

Consequences:

- The project preserves long-term ambition without making the initial build unbounded.
- MVP remains focused on digital tasks, review, ledger, and reputation.
- Architecture can leave room for ideas, groups, contribution events, and residual value later.

### 2026-06-09: Treat Adaptive Groups As Future Platform Layer

Decision:

Tadpole-style adaptive groups, alliances, public pledges, Builder tooling, and child-group royalties will be documented as future platform concepts, not MVP requirements.

Context:

The second old source emphasizes group evolution, group templates, public demand aggregation, leadership accountability, and group reproduction. These ideas could become central to Storm's long-term differentiation, but they depend on simpler group ownership, governance, and ledger behavior first.

Alternatives considered:

- Add group templates and public pledges to the MVP.
- Ignore the source because it overlaps with the previous old document.

Consequences:

- Storm keeps the adaptive organization concept visible.
- MVP remains focused on paid digital work execution.
- Future architecture can reserve names for group templates, group relationships, and pledges.

### 2026-06-09: Capture Creative Seeds As Long-Term Concept

Decision:

The "02.26 storm notes" source will be represented as the creative seed concept: early creative input that can grow into projects, tracked contributions, and residual value.

Context:

This source clarifies Storm's original emotional and economic thesis: latent creative ideas are underused, and creative input should be able to compound like an investment when others build on it.

Alternatives considered:

- Treat creative seeds as part of the MVP.
- Collapse the concept entirely into projects and tasks.

Consequences:

- Storm's vision now captures the idea-to-value ambition more directly.
- The MVP remains focused on project/task execution.
- Future domain modeling can decide whether creative seeds are separate entities or simply the earliest state of ideas.

### 2026-06-09: Define MVP As Crowdsourced Projects

Decision:

Storm's MVP is crowdsourced projects, not a generic work marketplace.

Context:

The user clarified that the first product should prove the crowdsourced project model. The endgame is that people can do all of their work through that model and the corporate paradigm ceases to matter as the default way to organize labor.

Alternatives considered:

- Frame the MVP as a freelance marketplace.
- Frame the MVP as project management software.
- Start directly with the full post-corporate work model.

Consequences:

- MVP language now centers projects, not isolated gig tasks.
- The first build must show collective project progress, not just task posting and completion.
- Long-term docs now explicitly describe Storm as a general work model that could make corporate employment optional or obsolete.

### 2026-06-09: Add AI Training Provenance To Long-Term Vision

Decision:

Storm should eventually allow AI training on Storm data, and later approved Protheus Labs ecosystem data, while preserving source provenance and compensating originators when downstream AI-generated value can be attributed.

Context:

The user clarified that AI makes the original Storm concept more important. AI systems can be trained on people's work and create value without compensating the people whose work produced the underlying capability. Storm should provide a different model where training access does not erase attribution.

Alternatives considered:

- Forbid AI training on Storm data.
- Allow AI training without source compensation.
- Treat AI training compensation as an MVP feature.

Consequences:

- AI training provenance is now part of the long-term product vision.
- MVP still focuses on crowdsourced projects, but should preserve source provenance in contribution and artifact records.
- Future architecture now reserves concepts for datasets, dataset source records, training runs, AI value events, and attribution entries.

### 2026-06-09: Define Storm As Contribution Stewardship, Not Traditional Ownership

Decision:

Storm should treat traditional ownership as a legal interface rather than the core product primitive. The deeper primitives are provenance, contribution rights, usage rights, governance, and value routing.

Context:

The user clarified that Storm mixes concepts associated with capitalism and communism. Contributors should be compensated for value creation, but no party should be able to use ownership to withhold value created by the network.

Alternatives considered:

- Model Storm assets as conventionally owned by project owners.
- Model every contributor as an equal owner with veto power.
- Avoid legal ownership questions entirely.

Consequences:

- Docs now describe contribution stewardship and non-withholding legal wrappers.
- Legal wrappers such as patents and businesses are treated as external interfaces that must preserve contributor value rights.
- Future work must define how forks, spinouts, patents, and businesses route value back to contributors.

### 2026-06-09: Plan Future Protheus/InfRing Network Substrate

Decision:

Storm may eventually transition to Protheus network primitives based on InfRing once InfRing v2 is complete and a single instance can operate as a network node.

Context:

The user clarified that Storm can later rely on the Protheus network and InfRing operating system primitives. Current InfRing public docs describe a deterministic, receipt-first runtime with Kernel authority, Orchestration coordination, Gateway boundaries, validation, observability, local-first user authority, and federated proof-carrying node signals.

Alternatives considered:

- Build Storm permanently as a centralized web platform.
- Make InfRing a dependency of the MVP.
- Defer all mention of Protheus/InfRing until implementation.

Consequences:

- MVP remains a conventional app.
- Architecture docs now preserve future receipt, node, and network concepts.
- Domain model reserves future concepts for network nodes and receipts.

### 2026-06-09: Capture Socioeconomic Thesis

Decision:

Storm will document its broader socioeconomic thesis: contribution-based value routing as an alternative to both ownership-dominated capitalism and centrally controlled communism.

Context:

The user clarified that the system is broken and that Storm is intended as an answer to the unresolved balance between late-stage capitalism and communism. The thesis is that verified contribution, provenance, review, and value routing can preserve incentives without allowing ownership or central authority to become a permanent extraction layer.

Alternatives considered:

- Avoid political-economic framing.
- Frame Storm only as a productivity or marketplace tool.
- Assert the thesis without operational tests.

Consequences:

- Docs now include a dedicated socioeconomic thesis.
- The thesis is connected to the operational MVP proof: crowdsourced projects must work in practice.
- Future positioning can be ambitious while still requiring evidence from real project execution.
