# Versioning And Forks

Part of Storm's inspiration is GitHub and open source work.

GitHub made it normal for useful work to happen in the open through issues, branches, commits, pull requests, reviews, forks, maintainers, and merge history. Storm should generalize that pattern beyond code.

The long-term idea is not "Storm is GitHub for everything." The idea is that open contribution needs durable primitives:

- Version history.
- Forks.
- Branches or alternate lines of work.
- Merge proposals.
- Review before merge.
- Conflict handling.
- Provenance.
- Attribution.
- Rights and value propagation.

Storm needs those concepts for crowdsourced projects. InfRing may need them as a lower-level subsystem.

## Why This Matters

Crowdsourced work needs a way to diverge without destroying trust.

A project may need to:

- Accept one contribution while rejecting another.
- Keep alternate story canon versions.
- Fork a project when governance breaks down.
- Spin out a business while preserving upstream value rights.
- Let a group experiment without erasing the parent lineage.
- Merge improvements back into the source project.
- Preserve who contributed what across forks and merges.

Without versioning and fork primitives, Storm will eventually rely on social authority or manual bookkeeping for exactly the areas where trust matters most.

## GitHub Inspiration

Useful GitHub-inspired ideas:

- Public issue/task coordination.
- Branches for work in progress.
- Commits as durable change records.
- Pull requests as reviewable merge proposals.
- Maintainers as accountable merge authorities.
- Forks as a freedom mechanism.
- History as evidence.
- Blame or authorship as provenance.
- Open source licenses as usage rules.

Storm should adapt these patterns, not copy them literally.

Stories, inventions, policies, datasets, research, designs, and organizations need versioning too, but their merge rules differ from code.

## InfRing Versioning/Fork Subsystem

InfRing may need a versioning and fork subsystem that can support Storm and other Protheus Labs applications.

Possible primitive concepts:

- Versioned object.
- Version node.
- Change operation.
- Branch.
- Fork.
- Merge proposal.
- Merge decision.
- Conflict record.
- Lineage edge.
- Contributor attribution.
- Policy attached to lineage.
- Receipt for version operations.

The subsystem should not assume the artifact is source code. It should support generic versioned project state and allow applets to define domain-specific merge behavior.

## Storm's Product Boundary

Storm should own the user-facing workflow:

- Task creation.
- Submission.
- Review.
- Applet-specific merge rules.
- Project governance.
- Value routing.
- Contributor experience.

InfRing should eventually own the primitive layer where practical:

- Version graph.
- Fork lineage.
- Receipt-backed changes.
- Merge evidence.
- Conflict records.
- Network replication.
- Local validation of incoming forks or merges.

Storm can keep product-facing projections for usability, but the canonical lineage should eventually come from the stronger primitive.

Versioning should expose a shared contract to applets. Applets define domain merge semantics; the versioning subsystem owns lineage records, fork records, merge proposal state, and receipt mapping.

## Native Bootstrap Path

Storm can start with simple native versioning:

1. Store submitted artifacts.
2. Mark accepted submissions.
3. Keep project export versions.
4. Track parent project id when a project is forked.
5. Preserve contribution and value lineage manually.

Story Forge MVP can stay simpler:

- Accepted submissions.
- Canon notes.
- Exported story package versions.
- No complex branching.
- No public fork marketplace.

Later, Storm can introduce:

- Project forks.
- Merge requests between forks.
- Applet-specific conflict handling.
- Branching story canon.
- Versioned datasets.
- Versioned value policies.
- Versioned governance rules.

## Forks And Value Routing

A fork must not erase upstream value.

When a project forks, Storm should preserve:

- Parent project lineage.
- Included contribution records.
- Contributor attribution.
- Applicable licenses or legal wrappers.
- Residual claims or value-policy obligations.
- Dataset and AI training provenance.
- Protocol origin allocation where applicable.

Forking should create freedom to continue work, not freedom to strip provenance.

## Merge Rules Are Applet-Specific

Storm core can provide a generic merge proposal workflow, but applets define what merge means.

Examples:

- Story Forge: merge a scene, lore entry, character note, or canon package.
- Code Forge: merge commits or patches after tests and review.
- Invention Forge: merge CAD files, prototype test data, or manufacturing notes.
- Research Forge: merge validated findings, source records, or analysis updates.
- Governance: merge policy changes after required approval.

This argues for InfRing providing the version graph and receipts while Storm applets provide domain merge semantics.

## Design Guardrails

- Forks must preserve provenance by default.
- Forks should not automatically grant permission to ignore upstream value rules.
- Merge decisions should be receipt-backed or audit-backed.
- Version history should be append-oriented.
- Applets should not invent incompatible lineage models when a common primitive can serve them.
- Private work can exist, but once it creates ledgered or governed value, the relevant lineage must be preserved.
- Versioning should not make the MVP heavy. Bootstrap records are enough until fork pressure appears.

## Open Questions

- Should InfRing versioning be content-addressed, operation-based, or hybrid?
- What is the minimal version node schema?
- How should generic lineage map to applet-specific artifacts?
- How should conflicts be represented outside source code?
- What is the first Storm-native fork model before InfRing support exists?
- How should value policies propagate through forks?
- Can a fork reject future governance changes from its parent?
- What does it mean to merge a story universe, invention, or organization?
- Should Code Forge use Git directly, InfRing versioning, or both?
- How should private forks later become public without losing provenance?
