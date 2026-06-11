# Legal Readiness Policy Template

This document defines a concrete policy schema for when legal obligations block or gate project actions.

The goal is not legal advice.
It is to make legal readiness explicit, auditable, and policy-driven so product and InfRing integration remain deterministic.

## Policy Template Shape

Use one policy per applet, jurisdiction, and release-phase where legal risk changes meaningfully.

Example fields:

- `policy_id`: stable machine ID.
- `applet`: applet slug (`story_forge`, `code_forge`, `invention_forge`, `general`).
- `jurisdiction`: default legal region hint.
- `version`: semantic version for the policy.
- `effective_from`: UTC timestamp.
- `effective_until`: optional UTC end timestamp.
- `default_gate`: fail-closed vs fail-open behavior when policy data is missing.
- `gates`: action-specific legal preconditions.

## Action Gate Fields

Each gate should include:

- `required_documents`: legal-document IDs that must exist.
- `required_filings`: filing classes that must be resolved.
- `proof_requirements`: accepted proof types and minimum fields.
- `fallback`: what happens when automated filing is unavailable.
- `waiver_rules`: who can waive, what limits apply, and required approval threshold.

## Canonical Gate Names (Initial)

Use these in the first legal gate policy:

- `project_launch`
- `payout_release`
- `dispute_resolution`
- `residual_crediting`
- `spinout_transition`
- `data_export_contract_required`

## Suggested Document Types

- `contributor_terms`
- `project_terms`
- `ip_assignment`
- `payment_acceptance`
- `residual_ack`
- `spinout_wrapper_request`

## Suggested Filing Types

- `business_registration`
- `tax_or_withholding_notice`
- `copyright_or_ip_notice`
- `platform_contract_notice`

## Proof Types

The policy can require one or more proofs:

- `provider_confirmation_id`
- `provider_status`
- `submission_payload_hash`
- `signed_artifact_hash`
- `uploaded_receipt`
- `manual_declaration`

Each proof entry should include:

- actor identity (`human`, `agent`, `system`),
- timestamp,
- immutable artifact pointer,
- source-of-truth string.

## Example Policy (Draft JSON)

```json
{
  "policy_id": "lp_story_forge_2026_1",
  "applet": "story_forge",
  "jurisdiction": "US",
  "version": "1.0.0",
  "default_gate": "fail_open",
  "gates": {
    "project_launch": {
      "required_documents": ["project_terms", "contributor_terms"],
      "required_filings": [],
      "proof_requirements": ["manual_declaration", "submitted_terms_hash"],
      "fallback": "notify_owner",
      "waiver_rules": {
        "allowed": false,
        "approver": ["owner", "protheus_admin"],
        "max_count": 0
      }
    },
    "payout_release": {
      "required_documents": ["project_terms", "ip_assignment", "payment_acceptance"],
      "required_filings": [],
      "proof_requirements": ["manual_declaration", "signed_artifact_hash"],
      "fallback": "hold_until_manual_submission",
      "waiver_rules": {
        "allowed": true,
        "approver": ["owner", "protheus_admin"],
        "max_count": 1
      }
    },
    "spinout_transition": {
      "required_documents": ["residual_ack", "spinout_wrapper_request", "ip_assignment"],
      "required_filings": ["platform_contract_notice", "business_registration"],
      "proof_requirements": ["provider_confirmation_id", "uploaded_receipt"],
      "fallback": "block_until_filed",
      "waiver_rules": {
        "allowed": true,
        "approver": ["governance_council", "protheus_admin"],
        "max_count": 2
      }
    }
  }
}
```

## Operational Rules

- Legal documents are not sufficient without matching filing proof when filing is required by policy.
- Proof is checked at transition time, not only at submission time.
- Manual proof capture must include uploader identity and retention timestamp.
- A failed filing may carry an exception state, but actions remain blocked until fixed unless waiver is approved.
- Every policy decision should attach:
  - policy ID,
  - policy version,
  - action attempted,
  - evaluated gate result,
  - missing requirements.

## Future Alignment to Receipts / InfRing

This policy template is designed to map cleanly to receipt-backed proof systems later:

- `required_documents` -> legal-document records.
- `required_filings` -> filing records.
- Proof fields -> canonical evidence IDs in compliance/audit receipts.
- Gate outcome -> policy-checked transition event that can be independently replay-verified.

## Initial Rollout Plan (Phase 5.6)

- Add this as a policy artifact first for Story Forge in a non-blocking mode.
- Expand to Code Forge once rights complexity is better understood.
- Tie payout release gate to at least `payment_acceptance` and `ip_assignment` in at-risk workflows.
- Evaluate adding tax/regulatory filing channels after manual workflow confidence is stable.
