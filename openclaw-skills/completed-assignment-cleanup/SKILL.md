---
name: completed-assignment-cleanup
description: Archive learner-confirmed submitted coursework without deletion.
---

# Completed Assignment Cleanup (OpenClaw)

Use only after the learner identifies the submitted artifact and requests cleanup. This is organization, not proof of upload or receipt. Check `academic-assignment-support` for learner authorship and AI-use boundaries if it is installed; otherwise read the current brief and project rules directly.

## Procedure

1. **Discover state.** Use OpenClaw `ls` on the root, `Resources/`, and existing `Archive/`; use `read` for workspace rules, brief, index, and AI-use record. For PDFs use `pdf` when available, and check its page limits. `read` does not extract binary DOCX; use a permitted parser/converter through `exec` if available, or report the gap. Identify the learner-reported submitted artifact, editable source, assessment project, original evidence, and protected backups. Do not infer a submission receipt from a filename.
2. **Classify without deletion.** Keep the reported submitted PDF, final editable source, original evidence, brief, workspace instructions, and disclosure intact. Move only superseded drafts, intermediate copies, scaffolds, and notes to `Archive/`. Respect protected backups and check for target-name collisions before each move.
3. **Move with verification.** Use OpenClaw `exec` for approved hash, directory-creation, and move commands appropriate to the active host. Record source hashes before moving; compare the destination files with those hashes afterward. Stop and report any failed move or mismatch. Preserve names and contents. Never rewrite the submitted artifact.
4. **Update status only within scope.** If authorized, use `read` then `edit` or `apply_patch` to update the project `README.md` and current workspace context (`AGENTS.md` if present). Identify the final artifact, root essentials, archived items, and learner-reported completion without claiming an independently checked receipt. Keep the disclosure accurate; do not rewrite assessed prose or copy identifiers into the agent's personal `USER.md` or `MEMORY.md`.
5. **Verify actual state.** Re-list root and archive with `ls`. Check each expected destination, absent source, hash, and preservation of final source/PDF. Open or parse relevant files with available tools. If an image link in an archived draft still points at root `Resources/`, say so. Report verification performed and any unavailable parser or receipt.

## Pitfalls

- Cloud sync or an editor may replace a file during cleanup. Recheck paths before moving.
- `Archive/` preserves provenance; it is not trash.
- An unreadable export or missing receipt does not justify claiming verification or submission.
