---
name: assignment-export-verification
description: "Use when verifying coursework PDF or DOCX exports."
version: 0.1.0
author: Hermes Agent
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [coursework, export, pdf, docx]
    related_skills: [academic-assignment-support, assessment-evidence-audit]
---

# Assignment Export Verification

Check that a report export reflects the learner's current source and meets the current brief. This procedure verifies an existing artifact; it does not author assessed text or imply that Moodle received it. Use `academic-assignment-support` for permissions and `assessment-evidence-audit` for a full requirement-to-image mapping.

## When to Use

- Learner has a Markdown, DOCX, or other editable report and wants its PDF/DOCX export checked before submission.
- Learner reports a new export may contain old text, broken images, split figures, or wrong dimensions.
- Do not overwrite a submitted artifact or protected original. If the requested source or export is unclear, identify it before touching files.

## Procedure

1. **Identify authority and versions.** Read workspace instructions, brief, the learner's current editable source, and the *exact* export with `read_file` and the relevant `pdf`/`docx` skill. Record expected filename and format, required image order/limits, and the latest learner-confirmed corrections. Distinguish a learner-reported submission from an independently checked file; keep historical exports separate.
2. **Compare content.** Check key changed passages in source against export text; an export can preserve an older draft. Enumerate headings, figure labels, embedded images, and their order in the export. Resolve Markdown links and verify that images actually appear in the exported document. Count all images, including those between numbered groups; do not infer count from filenames or figure labels alone. For a reported fresh export, render and inspect the exact file rather than trusting its timestamp alone. When prior page renders are available, compare their pixel hashes at the same rendering settings and compare extracted text; changed metadata can accompany an identical layout.
3. **Check rendered layout.** Inspect the exported pages for missing/blank images, broken links, split figures/captions, orphaned headings, clipped screenshots, and image size limits specified in the brief. Preserve aspect ratio when assessing or, only if explicitly authorized, changing dimensions. If the learner reports a viewer-only discrepancy after a successful check, inspect their attachment and independently rerender the affected page from the exact saved export. Compare the result with the original evidence before changing the document or reversing the export verdict. Source raster softness and unequal native image widths do not by themselves prove an export fault. If the discrepancy is absent from the independent render and source, describe a viewer/preview artefact as likely, not a diagnosed viewer bug. For DOCX inspect the saved package and embedded media, then request a real office-app open/render check when compatibility matters. A valid package alone does not prove Word renders it correctly.
4. **Handle failures within scope.** Report precise page/section and source/export discrepancy; an inspection request permits a findings report, not an edit. For an explicitly authorised repair, reread the current source immediately before repair and reuse any fixes already present. Edit only the user-designated working copy and preserve learner-authored prose. Back up the exact authorised source/export targets before changing them, without overwriting an existing backup. Complete the requested repair and deliver the repaired, verified artifact or report the specific blocker and checks still unverified. Regenerate through the actual export path when available. If using a direct Chromium export, identify that export route and verify the resulting PDF itself; this does not certify the VS Code extension's output.
5. **Verify again.** Reread and inspect the newly generated *exact* export after any fix. Recheck corrected text, figure/image count and order, page boundaries, and required filename/format. If the exporter or viewer cannot run, say which checks remain unverified. Do not claim an upload, submission, or grade without independent evidence.

## Pitfalls

- Correct source text does not prove the exported PDF contains it.
- An image link that resolves locally can still fail in the export; image presence must be checked in the output.
- PDF page count, DOCX package validity, and source hashes answer different questions; none alone proves visual correctness.
- Editing a final submission to repair layout is not a default step. Ask before any change, and leave submitted artifacts intact.

## Verification

Record the exact source and export checked. List observed content/layout results and any remaining gaps; claim success only for the artifact and export path actually inspected.
