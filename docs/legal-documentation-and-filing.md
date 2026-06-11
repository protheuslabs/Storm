# Legal Documentation And Filing

## Purpose

Storm eventually needs a dedicated subsystem that creates the legal artifacts required for compliant coordination and reward flows.

The goal is practical, bounded legal support:

- generate structured legal work products when possible,
- submit or trigger real filings when integrations exist,
- or notify users with required next actions when manual filing is still necessary,
- and gate certain workflow states until proof of filing is provided when required.

The subsystem is not a legal advice engine. It should provide protocol-level documentation, process automation, and compliance evidence trails.

## Early Positioning

In the MVP era, this remains out-of-scope except for basic attestation and provenance recording.

As Storm grows into higher legal/commercial phases, this becomes a growth subsystem.

- Phase 5: required legal forms for selected project categories.
- Phase 5.5: rights-sensitive workflows require stronger filing evidence.
- Phase 6: residual, business-forming, and spinout workflows require stronger legal routing.

## Core Responsibilities

1. Document generation

- Project terms, contributor role terms, and payout acceptance language.
- Residual or derivative-use policy summaries.
- IP/licensing statement templates.
- Collaboration agreements and consent records.

2. Filing orchestration

- Decide whether a filing is:
  - auto-generable,
  - delegatable through partner provider APIs,
  - or user-executed.
- Build and persist filing packets where possible.
- Capture filing attempts and responses.

3. User action and proof capture

- Notify users clearly when legal action is required on their side.
- Require explicit evidence before key state transitions where policy says required.
- Store proofs (reference numbers, document URLs, signed PDFs, signed hashes, timestamps, uploader identity).

4. Policy-gated workflow integration

- Associate legal requirements with projects, tasks, disputes, and payouts.
- Prevent payout or project lifecycle progression when required documents are missing.
- Keep the gating logic versioned in policy, not hardcoded.

## Suggested Record Model

- `LegalDocument`
  - template version
  - jurisdiction hint
  - involved users/projects/tasks
  - signature state
  - generation hash

- `LegalFiling`
  - filing target
  - provider or manual channel
  - status lifecycle (queued, submitted, accepted, rejected, pending-user-action, exempt)
  - proof artifact IDs
  - submission timestamps and response receipts

## Relationship To InfRing

This is a high-compatibility area for future receipt-backed proof systems:

- document templates and legal obligations can become shareable policy records,
- filing proof and filing responses can be represented as receiptable evidence,
- local policy can continue to decide if a state transition requires external proof.

## Why This Matters

Even with perfect contribution accounting, Storm cannot sustain real-world trust without legal closure points.

This subsystem:

- reduces hidden risk around ownership and downstream use,
- enables stronger trust signaling for enterprise and institutional usage,
- supports legal accountability without centralizing all legal control in a single org.

## Open Questions

- Which legal documents should be auto-generated versus manually signed?
- Which jurisdictions should be supported first?
- Which workflow transitions are legally blocked until documents are filed?
- What proof format is sufficient for automated trust (hash-only vs provider response)?
- What fallback exists for regions where no filing API exists?
