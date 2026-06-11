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

### 2026-06-10: Enforce Actor Parity for Users and Agents

Decision:

Storm should model humans and authorized agents against the same task-workflow mechanisms, with agents using a command/API transport that enforces the same task state transitions, review rules, payout policy, and audit events.

Context:

Users requested that agent swarm participation should be possible without creating a separate trust system from humans. Authorized agents should use the same principles as users, but expose a command-style interface (and eventually API) for automated execution.

Alternatives considered:

- Build two independent paths: one for humans and one for agents.
- Ban agents entirely to protect reputation integrity.
- Allow silent automation in exchange for post-hoc detection.

Consequences:

- Command execution should be an API transport, not a separate workflow authority.
- Core records like claim, submission, review, dispute, payout, and reputation stay unchanged for both actor types.
- Authorization should shift to explicit `agent authorization` + execution mode policy, rather than hidden capability assumptions.
- Product roadmap and subsystem docs now track the command API as a future integration layer.

### 2026-06-10: Add Legal Documentation And Filing Subsystem

Decision:

Storm should add a dedicated legal-documentation and filing subsystem that can generate required documents, submit where partner APIs exist, notify users for manual filing, and require proof records before legal-sensitive transitions.

Context:

As Storm scales into residual claims, spinouts, and higher-value workflows, legal closure points are required to reduce risk and improve trust.

Alternatives considered:

- Treat legal paperwork as one-off user notes.
- Delay legal workflows until enterprise integrations are built.
- Require legal actions before launch at the expense of MVP simplicity.

Consequences:

- Legal docs are treated as a future modular subsystem with template, filing, and proof-state records.
- Workflow transition gating should query legal state through policy, not hardcoded codepaths.
- Users can continue operating through a notification/manual filing workflow where automation is unavailable.
- Proof-of-submission artifacts become first-class audit inputs and future receipt inputs.

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

### 2026-06-09: Choose Story Forge As Proposed Initial Vertical

Decision:

Story Forge, a crowdsourced story creation system, is the proposed first Storm vertical.

Context:

The user suggested that enabling users to build crowdsourced stories would be a good initial vertical. Stories fit Storm's creative-seed thesis and test decomposition, subjective review, provenance, collaboration, and value routing without requiring physical logistics or highly regulated work.

Alternatives considered:

- Start with generic project types.
- Start with software projects.
- Start with operational work.

Consequences:

- MVP docs now point to Story Forge as the recommended narrow first category.
- Storm's underlying model remains generic.
- Story-specific tasks, canon, review, and artifact export become the first practical proof surface.

### 2026-06-09: Use Project Applets For Vertical Expansion

Decision:

Storm should expand through project applets: focused vertical workspaces that share Storm's generic foundation while keeping domain-specific complexity separated.

Context:

The user clarified that Story Forge, Code Forge, physical inventions, and other project types should be separated so Storm can start with the simplest applets first and only add complexity where necessary.

Alternatives considered:

- Put all vertical-specific behavior into Storm core.
- Build each vertical as a separate product with no shared substrate.
- Build generic project management only.

Consequences:

- Storm core owns projects, tasks, claims, submissions, review, disputes, reputation, ledger, and provenance.
- Applets own domain metadata, task templates, review rubrics, artifact types, merge behavior, and exports.
- Story Forge becomes the first applet rather than a one-off vertical.

### 2026-06-09: Add Release Switch Concept

Decision:

Storm should eventually support a release switch: a transition from Protheus Labs-operated platform to network-governed system once critical mass, trust, and infrastructure requirements are met.

Context:

The user clarified that if Storm succeeds, powerful governments and organizations may try to control or capture it because it challenges existing economic control structures. Storm may need to grow beyond control by any single organization. Protheus Labs can remain the origin point and collect transparent origin value permanently, but should not retain unilateral control after release.

Alternatives considered:

- Keep Storm permanently controlled by Protheus Labs.
- Release control immediately before trust and governance mature.
- Treat Protheus Labs value and Protheus Labs control as the same thing.

Consequences:

- Docs now separate origin value from control.
- Release switch is future scope, not MVP.
- Future governance must define release criteria, origin allocation, hidden-control audits, and emergency authority.

### 2026-06-09: Use InfRing Task Decomposition Long Term

Decision:

Storm can use its own early task decomposition helpers, but endgame decomposition should converge with InfRing's task decomposition primitive.

Context:

The user clarified that Storm will likely want to use InfRing's task decomposition. The InfRing repository already includes `execution:task-decompose`, task decomposition contracts, parallel micro-task execution, live handoff, and Rust execution code that emits task candidates with success criteria, routing, provenance, governance, and attribution metadata.

Alternatives considered:

- Build Storm's own permanent independent decomposition engine.
- Require InfRing task decomposition for the first MVP.
- Keep decomposition entirely manual forever.

Consequences:

- MVP may use manual tasks, static templates, or simple Storm-owned applet decomposition helpers.
- Storm-owned decomposition must stay behind a compatibility boundary.
- Applets can later provide domain constraints to InfRing.
- Storm will own economics, review, applet semantics, and value routing while InfRing becomes the canonical decomposition primitive.

### 2026-06-09: Separate Decomposition UI From Backend Decomposition

Decision:

Storm's task decomposition UI should be separate from temporary decomposition logic, which should live in the backend behind an interface.

Context:

The user clarified that task decomposition will need a UI, but temporary decomposition should be separate and backend-owned. This lets Storm build an applet-specific decomposition experience now while keeping a clean migration path to InfRing's task decomposition primitive later.

Alternatives considered:

- Put decomposition logic directly in the frontend.
- Skip decomposition UI until InfRing is ready.
- Couple Story Forge UI tightly to a temporary decomposition implementation.

Consequences:

- The UI owns input capture and candidate review.
- The backend owns temporary decomposition helpers, validation, run records, and future InfRing adapter calls.
- The same UI can survive the migration from Storm-owned decomposition to InfRing-backed decomposition.

### 2026-06-09: Use Readable Action Receipt IDs Backed By Structured Records

Decision:

Storm should use stable typed IDs and readable action receipt IDs that combine project ID, project action index, actor user ID, and a short digest.

Context:

The user suggested project IDs, user IDs, and action receipt IDs that are easy to read, with action receipt IDs combining project ID, user ID, and action order. This fits Storm's need for transparent audit trails, but the readable ID should not be the only source of truth.

Alternatives considered:

- Use opaque UUIDs only.
- Encode all receipt meaning only inside the ID string.
- Use global ordering only.

Consequences:

- IDs should be typed and stable.
- Project action indexes should be backend-allocated.
- Receipt records should store structured fields separately from the display ID.
- Receipt IDs should include a digest or hash component for tamper resistance and future InfRing mapping.

### 2026-06-09: Start Contribution Value Model As Transparent Policy

Decision:

Storm should calculate value from contributions through transparent, versioned value policies. The MVP should use fixed visible task values, while later versions can add contribution valuation for reviewers, coordination work, upstream creative seeds, residual value, and AI data value.

Context:

The user clarified that Storm will need a system that calculates value based on contributions. This is central to the product's thesis, but it is also one of the easiest areas to corrupt with opaque scoring, vague idea rent, or hidden manual authority.

Alternatives considered:

- Launch with a complex contribution-scoring algorithm.
- Let project owners manually decide every allocation.
- Split value equally across all visible contributors.
- Delay value modeling until residual compensation exists.

Consequences:

- MVP economics stay simple and trustworthy: fixed task value, review, payout, fee, adjustment.
- Value calculation becomes a policy layer separate from ledger recording and payment execution.
- Allocation explanations become a product requirement.
- Future residual, AI attribution, and network value routing can build on contribution records instead of replacing them.

### 2026-06-09: Treat Native Storm Mechanisms As Transitional When InfRing Has The Primitive

Decision:

Storm should use InfRing primitives wherever they become mature enough and phase out native Storm mechanisms that duplicate those primitives. Native Storm systems are acceptable for bootstrap, but overlapping native infrastructure should be interface-backed, auditable, and replaceable.

Context:

The user clarified that a goal is for Storm to later use InfRing primitives where possible and phase out its native mechanisms. This generalizes the earlier task decomposition decision into a broader architecture direction.

Alternatives considered:

- Build Storm as a permanent standalone substrate.
- Wait for InfRing before building Storm's product loop.
- Keep native and InfRing mechanisms permanently side by side.

Consequences:

- MVP can still be a conventional app.
- Native decomposition, receipts, audit logs, provenance, value-policy execution, ledger verification, and network trust should be designed as scaffolding where InfRing is expected to provide the stronger primitive.
- Storm should retain product semantics, applets, UX, value-policy authoring, legal wrappers, and marketplace behavior.
- InfRing should increasingly own lower-level execution, receipts, validation, node identity, deterministic policy, and network trust when those primitives are ready.

### 2026-06-09: Capture GitHub-Inspired Versioning And Fork Subsystem Need

Decision:

Storm should treat GitHub and open source work as inspiration for project versioning, forks, reviewable merge proposals, and durable provenance. InfRing may need a generic versioning/fork subsystem so Storm can eventually rely on shared lineage primitives instead of maintaining permanent Storm-only fork mechanics.

Context:

The user clarified that part of the inspiration is GitHub because it enables open source work, and that InfRing will need some versioning and fork mechanism, maybe as a subsystem. This matters because open contribution requires safe divergence, merge, authorship history, and fork lineage.

Alternatives considered:

- Treat forks as a Storm-only product feature.
- Assume Git is sufficient for all project types.
- Delay lineage modeling until after public forks exist.

Consequences:

- Storm docs now separate applet-specific merge semantics from the lower-level version/fork primitive.
- Storm can bootstrap with simple accepted submissions, exported versions, and parent project lineage.
- Future InfRing work should consider generic versioned objects, version nodes, forks, merge proposals, conflict records, lineage receipts, and policy propagation.
- Forks must preserve upstream provenance and value obligations rather than becoming a way to strip contributors from the history.

### 2026-06-09: Add Originality And Rights Enforcement As Future Subsystem

Decision:

Storm should eventually include an originality and rights-enforcement subsystem that helps prevent users from plagiarizing other Storm contributors or importing externally owned work without permission. AI can assist with similarity search, source matching, license analysis, prior-art research, and evidence summaries, but high-impact enforcement should be explainable, reviewable, and appealable.

Context:

The user clarified that Storm will need a mechanism to stop plagiarism and unauthorized use of legally owned work. This is especially important if Storm supports open contribution, forks, residual value, AI training datasets, story worlds, code, inventions, and exported project artifacts.

Alternatives considered:

- Treat plagiarism as only a manual dispute issue.
- Let AI automatically reject or punish users.
- Delay rights enforcement until after legal wrappers exist.

Consequences:

- Automated originality and rights enforcement remains out of MVP.
- MVP should still preserve provenance and contributor attestations so later checks have evidence.
- Later Storm should model rights source records, originality checks, similarity matches, rights reviews, and enforcement actions.
- The subsystem should avoid false-positive abuse by requiring evidence, review, and dispute paths.
- Some rights evidence may eventually map to InfRing receipts or validation signals.

### 2026-06-09: Keep Storm Subsystems Modular

Decision:

Storm's major subsystems should remain modular behind explicit contracts, even if the first implementation is a monolith.

Context:

The user clarified that Storm subsystems should stay modular. This matters because Storm will accumulate many powerful mechanisms: applets, decomposition, review, value policy, ledger, reputation, versioning, rights enforcement, AI provenance, payments, governance, and InfRing adapters.

Alternatives considered:

- Build each feature directly into one large workflow service.
- Split into microservices before the MVP proves the product loop.
- Let each applet implement its own versions of shared platform primitives.

Consequences:

- The first implementation can stay simple, but code and data boundaries should be explicit.
- Subsystems should own their canonical records and expose contracts or events.
- Applets should define domain semantics without bypassing shared platform subsystems.
- Provider interfaces make it easier to replace native mechanisms with InfRing primitives later.
- Contract tests become important before subsystems grow complex.

### 2026-06-10: Add Practical Subsystem Inventory

Decision:

Storm should track a practical subsystem inventory alongside the visionary subsystems. The missing or underdeveloped areas include workflow orchestration, identity and roles, artifact storage, review/dispute, payments and compliance, fraud/risk, search and matching, notifications, policy engine, audit/event bus, privacy/consent, and API/integration boundaries.

Context:

The user asked whether any subsystems were missing. The existing docs covered major visionary pieces such as decomposition, value routing, rights enforcement, versioning, AI provenance, applets, and InfRing migration, but several practical product subsystems needed to be called out explicitly.

Alternatives considered:

- Leave these as implementation details.
- Fold practical subsystems into the broad modularity doc only.
- Document only future InfRing-facing mechanisms.

Consequences:

- Storm now has a subsystem inventory with MVP-critical, early-platform, growth, and future-substrate categories.
- The first build should prioritize workflow orchestration, identity/permissions, project/task core, review/dispute basics, ledger, basic reputation, Story Forge, artifact storage, and audit/events.
- Growth subsystems such as payments/compliance, fraud/risk, search/matching, privacy/consent, and integrations are documented before they become urgent.
- The inventory gives implementation a map without forcing premature microservices.

### 2026-06-10: Add Agent Participation And Bot Control

Decision:

Storm should eventually allow AI agents and automation through explicit authorized channels, while preventing unauthorized bots from pretending to be human contributors, reviewers, or governance participants.

Context:

The user clarified that Storm will need a way to make sure unauthorized bots are not doing user tasks. Agents can be allowed when they come through the right channels, but they should not impersonate humans.

Alternatives considered:

- Ban agents entirely.
- Allow agents without disclosure.
- Treat all bot detection as a generic fraud concern.

Consequences:

- Storm should model execution modes such as human-only, human-assisted, agent-assisted, and authorized agent execution.
- Future domain records now include agents, agent authorizations, and agent sessions.
- MVP does not need sophisticated bot detection, but task terms and submission records should avoid assuming every task was purely human.
- Reputation, payout, review, rights enforcement, and InfRing receipt mapping should eventually account for disclosed versus undisclosed automation.

### 2026-06-10: Use Story Forge As Public Wedge

Decision:

Storm should preserve the broad internal platform thesis, but the first public product should lead with Story Forge as the concrete wedge.

Context:

Product feedback clarified that Storm is best framed internally as a coordination, attribution, and value-routing layer for crowdsourced work. That framing is strategically useful, but too abstract for the first market-facing promise. Story Forge gives the product an understandable entry point: collaboratively create stories through paid, reviewable creative tasks.

Alternatives considered:

- Lead publicly with the full post-corporate economic vision.
- Pitch Storm as a generic crowdsourced project marketplace.
- Hide the Storm platform thesis entirely and only talk about Story Forge.

Consequences:

- Storm docs now separate internal platform positioning from the first public wedge.
- Story Forge becomes the recommended first product promise.
- The first MVP should prove Storm primitives under a story-specific interface.
- Broader Storm messaging can expand after real usage validates task decomposition, review, reputation, provenance, ledger, and dispute mechanics.

### 2026-06-10: Capture Protheus Ecosystem Thesis

Decision:

Storm should document its role inside the broader Protheus human-AI coordination network: Storm is the contribution, attribution, review, reputation, dispute, rights, and value-routing memory layer.

Context:

Additional product discussion clarified that Protheus products are not merely separate apps. Each product can be a useful wedge that also captures structured, consented, provenance-rich activity for a broader network. Lycium, Storm, PQTS, Lensmap, and InfRing each represent different coordination surfaces. Storm is especially important because it can make the ecosystem non-extractive by preserving who did what, who reviewed it, what rights apply, what agent participation occurred, and how value should flow back.

Alternatives considered:

- Treat Storm as only a standalone marketplace.
- Describe Protheus products as apps that feed a central lab.
- Keep the ecosystem thesis informal until after implementation.

Consequences:

- Docs now frame Protheus as human-AI coordination infrastructure.
- Storm's long-term ecosystem role is explicit without changing the Story Forge MVP wedge.
- The docs distinguish founding stewardship and origin value from hidden platform ownership.
- Future architecture must account for consent, portability, cross-product provenance, anti-capture governance, and release-switch credibility.

### 2026-06-10: Define Idea Workspace Then Invite, Then Match

Decision:

Storm should support a staged execution model: private idea workspace and solo work first, manual invite-based collaboration second, and algorithmic matching only after stable task decomposition and access controls.

Context:

The user clarified that Storm should be useful for individuals storing and developing ideas, with solo workflow treated as a first-class path. Collaboration should initially be explicit and invite-driven before matching systems expand participation, and this should feed into Story Forge as the first applet.

Alternatives considered:

- Require project posting and matching at launch.
- Keep everything invite-only indefinitely.
- Start with public matching and defer solo workflows indefinitely.

Consequences:

- MVP should include idea capsules, private drafting, and explicit invite mechanics.
- Matching remains future scope and should be gated by project/task quality criteria.
- Product docs now separate workflow readiness from long-term matching automation.
- Story Forge and other applets should inherit this staged model to keep trust and complexity in check.

### 2026-06-10: Add Delivery Management As Future Applet Layer

Decision:

Storm should eventually support strong project-management capabilities comparable to Linear, Airtable, and Jira, with planning, milestones, dependencies, templates, and reporting becoming first-class delivery management features in later phases.

Context:

The user indicated the system needs to become a full project management system over time, not just a marketplace. Story-level task execution and payout mechanics are still the MVP foundation, but stronger planning and team delivery workflows are required for long-term adoption.

Alternatives considered:

- Keep Storm scoped to tasks only and rely on external PM tools indefinitely.
- Treat PM features as unstructured metadata from day one.
- Build PM features before validating crowdsourced task/review economics.

Consequences:

- Storm documentation now includes delivery planning and PM capabilities as a growth track.
- MVP remains focused on task proof and private-to-invite workflows.
- A delivery-management applet is added to the applet sequence for later phases.
