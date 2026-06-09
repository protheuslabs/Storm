# Originality And Rights Enforcement

Storm eventually needs a mechanism that prevents users from plagiarizing other users or importing work that is legally owned elsewhere without permission.

This should be treated as an originality and rights-enforcement subsystem.

The subsystem should not pretend to be a final court of law. It should detect risk, assemble evidence, route suspicious cases into review, and prevent obviously copied or incompatible work from contaminating projects, ledgers, datasets, forks, and downstream value claims.

## Core Principle

Storm should protect contributors from having their work stolen, and it should protect projects from accidentally building on work they do not have the right to use.

That means Storm must care about:

- Plagiarism from other Storm contributors.
- Copying from outside copyrighted works.
- Unauthorized reuse of licensed material.
- Patent or prior-art risk for invention projects.
- AI-assisted paraphrase that hides a source.
- Provenance stripping across forks, datasets, and exports.
- False accusations that block legitimate work.

## Why AI Helps

AI may make this easier than it was when the original Storm concept was developed.

Useful AI-assisted techniques may include:

- Semantic similarity search.
- Embedding-based source matching.
- Near-duplicate detection.
- Code clone detection.
- Style, structure, and plot similarity analysis.
- Citation and source-consistency checks.
- Media fingerprinting for images, audio, and video.
- Patent and prior-art search assistance.
- License and policy compatibility analysis.

AI should support review, not replace it. Similarity is evidence, not a legal conclusion.

## Subsystem Responsibilities

The originality and rights-enforcement subsystem should:

- Maintain a source corpus of Storm-native work.
- Track source records from approved external inputs.
- Record licenses, permissions, and usage restrictions.
- Scan submissions before or during review.
- Compare new work against internal and external reference sets.
- Produce risk scores with evidence.
- Explain which sources triggered concern.
- Route risky submissions into review or quarantine.
- Hold payout or merge until rights risk is resolved.
- Preserve audit trails and receipts.
- Support contributor disputes and appeals.

## What The Subsystem Is Not

It is not:

- A complete legal department.
- A guarantee that no infringement exists.
- A reason to ban users based on unexplained AI output.
- A replacement for project terms, licenses, or human review.
- A tool for powerful users to suppress legitimate derivative or fair-use work without evidence.

Storm should be especially careful with false positives. A system designed to stop theft can become a censorship or gatekeeping tool if it is not transparent and appealable.

## Source Corpus

The subsystem should be able to compare against multiple source types.

Internal sources:

- Storm submissions.
- Accepted project artifacts.
- Rejected but protected submissions.
- Ideas and creative seeds.
- Story canon records.
- Dataset source records.
- Forked project lineage.
- Versioned exports.

External sources:

- Public web pages.
- Licensed reference libraries.
- Public-domain works.
- Open-source repositories.
- Patent databases and prior-art sources.
- User-provided source material.
- Partner or Protheus Labs ecosystem records.

External coverage will never be perfect. The subsystem should record which corpora were checked and which were not.

## Risk Signals

Possible risk signals:

- Exact text or code overlap.
- Near-duplicate passages.
- Unusually high semantic similarity.
- Shared plot, character, or worldbuilding structure.
- Reused variable names, comments, or commit patterns.
- Missing required citation.
- License incompatibility.
- Source copied from a disallowed domain.
- AI output that closely tracks a known source.
- Repeated similarity issues from the same user.
- Suspicious fork or dataset provenance changes.

Signals should be explainable. A reviewer should be able to inspect why the subsystem flagged the work.

## Enforcement Actions

Possible actions:

- Allow.
- Allow with attribution or citation.
- Request contributor explanation.
- Request revision.
- Quarantine submission.
- Block merge.
- Hold payout.
- Reject submission.
- Open dispute or rights review.
- Escalate for legal review.
- Remove infringing material from project artifacts.
- Penalize repeated bad-faith infringement.

High-impact actions should require review evidence, not only a model score.

## Rights Review Workflow

A rights review should answer:

- What submitted work is being evaluated?
- What source or sources triggered the concern?
- What evidence supports similarity or rights conflict?
- Was the contributor allowed to use the source?
- Is attribution required?
- Is the license compatible with the project?
- Does the project need revision, rejection, quarantine, or legal review?
- Does the contributor dispute the finding?
- What happens to payout, reputation, and contribution records?

Every rights review should create an audit trail.

## Relationship To Provenance

Originality enforcement depends on provenance.

Storm cannot reliably detect theft if it does not know:

- Who created the source work.
- When the source work entered Storm.
- Which project, task, fork, dataset, or export used it.
- What license or permission applied.
- Whether later work depended on it.

This makes originality enforcement tightly connected to contribution events, receipts, versioning, forks, dataset manifests, and value policies.

## Relationship To AI Training

AI training creates a second rights surface.

The subsystem should help detect:

- Training data added without permission.
- Dataset records missing source provenance.
- AI-generated outputs too similar to protected sources.
- AI-assisted rewrites that hide source dependency.
- Attempts to use AI as a laundering step for copied work.

If AI outputs become Storm contributions, they should carry upstream provenance when known.

## Relationship To InfRing

Originality and rights enforcement can begin as a Storm subsystem.

Long term, parts of it may map to InfRing primitives:

- Receipt-backed source records.
- Version and fork lineage.
- Dataset provenance receipts.
- Rights-review evidence bundles.
- Deterministic policy checks for license compatibility.
- Local validation of incoming network artifacts.
- Quarantine signals exchanged between nodes.

Storm should own product policy and user experience. InfRing may eventually provide lower-level evidence, receipts, validation, and network trust signals.

The subsystem should expose a clear contract to the rest of Storm. Other modules should request checks, consume risk results, and respond to enforcement events; they should not reach directly into the subsystem's evidence or review records.

## MVP Implication

The first MVP should not attempt automated legal enforcement.

It can still prepare by:

- Capturing contributor attestations of originality or permission.
- Preserving submission timestamps and artifact provenance.
- Recording source links when a task requires reference material.
- Keeping accepted and rejected submissions attached to users and tasks.
- Supporting manual disputes over copied work.

Automated scanning, external corpus matching, and rights review queues should come later.

## Open Questions

- What counts as plagiarism inside Storm by project type?
- Which external corpora should be checked first?
- How should Storm avoid exposing private submissions during similarity checks?
- How should false positives affect contributor reputation?
- When should payout be held for rights review?
- How should Story Forge detect copied plots, characters, lore, or prose?
- How should Code Forge integrate with open-source license scanning?
- How should Invention Forge treat patent and prior-art risk?
- How should AI-generated submissions disclose prompts, sources, and model usage?
- Which rights enforcement records should become InfRing receipts?
