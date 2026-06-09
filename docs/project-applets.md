# Project Applets

Project applets are Storm's expansion pattern.

Storm should provide a shared project substrate, then layer focused project-type applets on top. Each applet can add domain-specific fields, task templates, workflows, review criteria, artifact types, and export formats without contaminating the generic Storm core.

## Core Principle

Keep the foundation generic. Add complexity only inside the applet that needs it.

The shared foundation should handle:

- Projects.
- Tasks.
- Claims.
- Submissions.
- Reviews.
- Disputes.
- Reputation.
- Value ledger.
- Contribution events.
- Provenance.
- Permissions.

Applets should handle:

- Domain-specific project setup.
- Domain-specific task templates.
- Domain-specific artifact types.
- Domain-specific review rubrics.
- Domain-specific merge/export flows.
- Domain-specific vocabulary.

In later versions, applets may also provide decomposition constraints to InfRing. InfRing can propose decomposed tasks, while the applet decides which domain-specific templates, artifacts, and review rules apply.

Before InfRing integration is ready, an applet can include its own simple decomposition helper. That helper should be treated as temporary or adapter-backed, not as a permanent decomposition authority.

## Why Applets

Different project types have different complexity.

A story project needs canon, scenes, characters, lore, editorial review, and story-package export.

A code project needs issues, branches, commits, tests, CI, dependency risk, and code review.

A physical invention needs parts, prototypes, CAD files, materials, safety checks, manufacturing constraints, and patent provenance.

Trying to force every project type into one generic UI would either make the core too vague or make every project inherit complexity it does not need.

Applets let Storm start simple and grow deliberately.

## Initial Applet Sequence

Suggested order:

1. Story Forge: crowdsourced stories and narrative worlds.
2. Code Forge: crowdsourced software projects.
3. Game Forge: game design, narrative, assets, and mechanics.
4. Research Forge: source-backed research and synthesis projects.
5. Invention Forge: physical inventions, prototypes, CAD, and manufacturing paths.
6. Organization Forge: groups, alliances, and business spinouts.

The exact order should change based on traction, but the principle should stay: start with the simplest applets that prove the core model.

## Applet Contract

Every applet should define:

- Project metadata.
- Task types.
- Acceptance criteria templates.
- Submission artifact types.
- Review rubric.
- Merge or acceptance model.
- Export or delivery format.
- Applet-specific risks.
- What remains handled by Storm core.

## Storm Core vs Applet Boundary

Storm core should not know what a scene, pull request, CAD file, or research claim means unless that concept has become generic enough to serve multiple applets.

The applet owns domain semantics. Storm core owns coordination and economics.

Examples:

- Story Forge owns canon status.
- Code Forge owns test status and commit references.
- Invention Forge owns prototype stage and materials.
- Storm core owns task status, claim status, review status, ledger entries, and reputation events.

## Applet Maturity Levels

### Level 0: Template Pack

The applet is only task templates, labels, and project metadata.

### Level 1: Guided Workflow

The applet has a setup flow, task generator, and review rubric.

### Level 2: Domain Artifacts

The applet supports structured artifacts, previews, exports, or integrations.

### Level 2.5: InfRing Decomposition

The applet can send project goals and domain constraints to InfRing task decomposition and receive structured task candidates.

### Level 3: Domain Merge

The applet can merge accepted contributions into a coherent project artifact.

### Level 4: Domain Economy

The applet supports domain-specific residual value, licensing, or downstream monetization.

## First MVP Implication

Story Forge should probably start at Level 1:

- Story project setup.
- Story task templates.
- Story-specific review criteria.
- Simple accepted-submission flow.
- Simple story export or project package.

It should not start with full canon branching, residual royalties, AI story ownership, or publishing rights.

## Design Guardrails

- Do not put every applet feature into Storm core.
- Do not build applets before the core project loop works.
- Do not support too many applets before one applet proves completion.
- Keep applet data portable and provenance-preserving.
- Let successful applet concepts graduate into core only when multiple applets need them.
