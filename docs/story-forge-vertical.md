# Story Forge Vertical

Story Forge is the proposed first Storm project applet: a crowdsourced story creation system.

It lets users create story projects, break them into clear creative tasks, work in a private first pass, invite contributors manually, review submissions, and route value transparently.

Story Forge should prove the applet model. Storm core should handle projects, tasks, review, ledger, reputation, and provenance; Story Forge should add only story-specific metadata, task templates, canon handling, editorial review criteria, and story artifact export.

The first Story Forge MVP can use manually created story tasks, static templates, or a lightweight Story Forge decomposition helper. It starts as a private draft workspace, then supports invite-only collaboration, then later can add matching. Story Forge should then merge that decomposition path with InfRing task decomposition so a story premise and constraints become receipted candidate tasks such as scene drafts, character profiles, line edits, and continuity reviews.

## Public Wedge

Story Forge should be the first public wedge for Storm.

Storm's full vision is broad and infrastructure-heavy. Story Forge gives users a clear first promise: turn a story idea into paid, claimable, reviewable creative tasks and merge accepted work into a shared story artifact.

The product should feel like a story creation workspace first. Storm's generic project, review, reputation, ledger, and provenance primitives should be present, but they should not be the first thing a new user has to understand.

## Why Stories First

Stories are a strong initial vertical because they exercise Storm's core model without requiring physical logistics, regulated labor, or complex enterprise procurement.

Story projects naturally require:

- Creative seeds.
- Decomposition.
- Many kinds of contribution.
- Review and editorial judgment.
- Provenance.
- Versioning.
- Contributor reputation.
- Potential residual value.
- AI training provenance later.

They also create artifacts people understand: short stories, novels, comics, scripts, game narratives, lore worlds, interactive fiction, and serialized universes.

## MVP Thesis

If Storm can coordinate a crowdsourced story project from concept to publishable artifact, then it proves the core crowdsourced project loop in a culturally legible domain.

Story Forge should prove:

- A story idea can become a structured project.
- Creative work can be decomposed into claimable tasks.
- Contributors can complete bounded creative work.
- Editors or reviewers can evaluate submissions.
- The project can merge accepted contributions.
- The ledger can show who created what value.

## Story Project Types

Initial project types:

- Short story.
- Serialized fiction.
- Novel outline.
- Screenplay.
- Comic script.
- Game narrative.
- Worldbuilding bible.
- Character pack.
- Lore expansion.

The first MVP should pick one or two of these rather than support every format.

## Task Types

Story Forge tasks may include:

- Premise refinement.
- Plot outline.
- Chapter outline.
- Scene draft.
- Dialogue pass.
- Character profile.
- Setting description.
- Worldbuilding entry.
- Continuity review.
- Line edit.
- Tone pass.
- Sensitivity or audience review.
- Lore consistency review.
- Cover brief.
- Summary or pitch copy.

## Acceptance Criteria Examples

Story tasks need subjective judgment, but they still require criteria.

Examples:

- Scene draft must follow the assigned outline beat.
- Dialogue pass must preserve plot events and character intent.
- Character profile must include motivation, conflict, voice, relationships, and arc.
- Continuity review must identify contradictions with source canon.
- Line edit must preserve meaning while improving clarity, rhythm, and grammar.
- Worldbuilding entry must match established tone and not contradict locked canon.

## Roles

Story Forge can start with the same core Storm roles:

- Project owner.
- Contributor.
- Reviewer.
- Admin or resolver.

Story-specific names may include:

- Creator.
- Writer.
- Editor.
- Continuity reviewer.
- Lore steward.
- Producer.

The data model should keep generic Storm roles underneath the story-specific labels.

## Workflow

1. Creator starts a story project with premise, genre, target format, tone, and audience.
2. Creator or coordinator creates initial story tasks.
3. Contributors claim tasks.
4. Contributors submit drafts, edits, reviews, or lore artifacts.
5. Reviewers approve, reject, or request changes.
6. Accepted contributions become part of the project canon or draft.
7. Ledger records task value and contributor/reviewer allocation.
8. Project exports a story artifact or structured story package.

## Canon And Merge

Story Forge needs a concept of canon.

Accepted contributions may be:

- Merged into canon.
- Accepted as draft material.
- Accepted as alternate version.
- Rejected.
- Archived as reference.

The MVP can keep this simple with accepted submissions and project notes. Later versions may need branching, merging, canonical lore records, and versioned story packages.

GitHub is a useful analogy here, but story artifacts need their own merge semantics. A later Story Forge can support branches, alternate canon, forked universes, and merge proposals while preserving upstream contribution and value lineage. The generic version and fork mechanics should eventually come from a shared substrate, ideally InfRing, while Story Forge owns what it means to merge story canon.

## Why This Tests Storm

Story Forge tests the hardest Storm questions in a lower-risk domain:

- How do you reward idea originators without over-taxing execution?
- How do you evaluate subjective work fairly?
- How do you merge many contributors into one coherent artifact?
- How do you track provenance across creative fragments?
- How do you detect copied prose, characters, lore, or plot structures?
- How do you prevent contributors from being erased when a story becomes valuable?
- How do you let AI help without stealing contributor value?

## Initial Contribution Value

Story Forge should start with fixed visible task values.

Examples:

- Scene draft: fixed payout after approval against the assigned beat and acceptance criteria.
- Character profile: fixed payout after approval and merge into project materials.
- Line edit: fixed payout after approval.
- Continuity review: fixed reviewer or contributor payout based on review completeness.
- Worldbuilding entry: fixed payout if accepted into draft material or canon notes.

Later Story Forge can test limited upstream and residual value. A creative seed, plot outline, lore entry, or reusable review rubric may deserve downstream value when later work depends on it, but the first version should cap these claims and require concrete provenance.

## Out Of Scope For First Story Forge MVP

- Full residual royalties.
- Automated publishing.
- AI-generated story ownership rules.
- Film, game, or merchandise licensing.
- Complex canon branching.
- Full copyright and patent automation.
- Automated plagiarism and external-rights enforcement.
- Multi-project shared universes.
- Marketplace discovery beyond the initial project loop.

## Initial Success Metrics

- Number of story projects created.
- Percentage of story projects with at least five tasks.
- Percentage of tasks claimed.
- Percentage of claimed tasks submitted.
- Percentage of submissions approved.
- Time from task creation to accepted contribution.
- Number of accepted contributors per story.
- Reviewer agreement rate.
- Contributor repeat rate.
- Completed story artifacts exported.

## Strategic Value

Story Forge can be Storm's Falcon 1.

It is narrow enough to build, culturally understandable, and close to the original creative-seed thesis. If it works, Storm can expand from stories into games, films, software, research, products, and eventually broader work categories.

It also keeps the public pitch disciplined. The first release can talk about collaborative story creation while quietly proving the more consequential Storm substrate underneath.

## Applet Boundary

Handled by Storm core:

- Project status.
- Task status.
- Claims.
- Submissions.
- Reviews.
- Disputes.
- Ledger entries.
- Reputation events.
- Contribution provenance.

Handled by Story Forge:

- Story premise.
- Genre.
- Format.
- Tone.
- Target audience.
- Canon notes.
- Story task templates.
- Editorial review criteria.
- Story package export.

Future InfRing integration:

- Story Forge supplies premise, format, genre, canon notes, and target artifact.
- InfRing proposes decomposed task candidates.
- Story Forge applies story-specific templates and review rubrics.
- Storm records accepted tasks, provenance, and value rules.
