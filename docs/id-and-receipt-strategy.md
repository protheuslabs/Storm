# ID And Receipt Strategy

Storm needs IDs that are easy for humans to read and precise enough for machines to verify.

The core idea is right: project IDs, user IDs, and action receipt IDs should make it easy to understand where an action happened and who performed it. Action receipt IDs can combine project ID, user ID, and an action index.

However, readable IDs should be locators, not the only source of truth. Every receipt should also store structured fields and a digest so the system can verify what happened even if a readable ID is copied, truncated, or displayed out of context.

## ID Principles

- IDs should be stable.
- IDs should have type prefixes.
- Human-readable receipt IDs should be easy to inspect.
- Canonical records should store fields separately, not only inside the ID string.
- Receipt IDs should include an ordering component.
- Ordering must be allocated by the backend, not trusted from clients.
- Receipts should include a digest or hash of canonical receipt contents.
- Public IDs should avoid leaking sensitive private information.

## Suggested Prefixes

- `usr_`: user.
- `prj_`: project.
- `tsk_`: task.
- `sub_`: submission.
- `rev_`: review.
- `led_`: ledger entry.
- `act_`: action.
- `rcp_`: receipt.
- `dec_`: decomposition run.
- `tcd_`: task candidate.

## Project IDs

Project IDs should be stable and portable.

Suggested shape:

`prj_<short-ulid-or-slug>`

Examples:

- `prj_storyforge001`
- `prj_01JZ8V6F3QK4A9W2M6D5T8R7P0`

The display name can be human-friendly, but the project ID should remain stable even if the title changes.

## User IDs

User IDs should be stable and separate from display names or handles.

Suggested shape:

`usr_<short-ulid>`

Handles can change. User IDs should not.

For public receipts, Storm may eventually need a public contributor ID that is separate from private account identity.

## Action Index

Each project should maintain an append-only action index.

Suggested fields:

- `project_id`.
- `action_index`.
- `actor_user_id`.
- `action_type`.
- `created_at`.

The action index should be allocated transactionally by the backend.

Recommended format:

`000001`, `000002`, `000003`

This makes receipts easier to scan and gives each project a readable event timeline.

## Action Receipt ID

An action receipt ID can combine project, user, action index, and a short digest.

Suggested shape:

`rcp_<project-id>_<action-index>_<user-id-short>_<digest-short>`

Example:

`rcp_prj_storyforge001_000042_usr_7KQ9M2_ab12cd`

Why include a digest:

- Prevents two similar-looking receipts from being treated as equivalent.
- Helps detect tampering.
- Makes receipt IDs safer across exports, forks, and network replication.

## Canonical Receipt Fields

Every receipt should store:

- receipt id.
- project id.
- action index.
- actor user id.
- action type.
- target type.
- target id.
- payload hash.
- previous receipt id.
- created at.
- source system.

Future receipts may also store:

- node id.
- signature.
- policy version.
- validation status.
- InfRing receipt id.
- parent receipt ids.

## Receipt Chain

Receipts should be chainable.

Each project action receipt can reference the previous project receipt:

- `previous_receipt_id`.
- `previous_receipt_hash`.

This creates a project-level action chain that is easy to audit and can later map to InfRing receipt-backed execution.

## Ordering Caveats

Ordering is useful but dangerous if oversimplified.

Storm should distinguish:

- Project action order.
- User action order.
- Ledger order.
- Network receipt order.
- Wall-clock time.

The same action may appear in multiple orders depending on context. The project action index should not be treated as the only global ordering source.

## MVP Recommendation

For MVP, implement:

- Stable project IDs.
- Stable user IDs.
- Project-scoped action indexes.
- Readable action receipt IDs.
- Structured receipt records.
- Payload hashes.

Do not implement:

- Cryptographic signatures.
- Network receipt consensus.
- Full InfRing receipt integration.
- Public/private identity separation beyond basic user IDs.

Those can come later once the core project loop works.
