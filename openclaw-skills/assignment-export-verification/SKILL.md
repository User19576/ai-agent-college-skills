---
name: assignment-export-verification
description: Check a coursework export against its editable source.
---

# Assignment Export Verification (OpenClaw)

Verify an existing report export without authoring assessed prose or inferring submission. Check `academic-assignment-support` and `assessment-evidence-audit` if installed; otherwise read the current brief and project rules directly.

## Procedure

1. **Identify versions.** Use OpenClaw `ls` and `read` for the current editable text source and instructions. Use the native `pdf` tool for a PDF brief/export, checking its page, size, and partial-result limits. `read` refuses binary DOCX content: use an approved available parser or converter through `exec` for DOCX extraction and rendering. If none is available, report the unverified DOCX checks instead of asserting equivalence. Record exact filenames, required format, image order/limits, and latest learner-confirmed corrections.
2. **Compare content.** Match key source passages against actual export text; an export can contain an older draft. Resolve Markdown image links relative to the editable file. Count every embedded image, heading, and figure label in the export, including images between numbered groups. A filename or link alone does not show that an image survived export.
3. **Inspect pages.** Use `view_image` on actual rendered PDF/DOCX pages or available images extracted from the exact export. If the available `pdf` result omitted pages, render or extract those pages with an approved tool through `exec`. Check missing or blank images, split figures/captions, orphan headings, clipping, and physical image limits from the brief. A DOCX package opening or plain-text comparison is not a visual render; request an office-app check when compatibility matters.
4. **Handle discrepancies only within authorization.** Cite the page/section and source/export mismatch. Edit only the learner-designated working copy using `edit` or `apply_patch` when authorized; back up originals before embedded-image changes. Preserve assessed prose and do not overwrite submitted artifacts. Regenerate with the actual exporter when available: a separate Chromium render is not proof of a VS Code Markdown PDF export.
5. **Verify the exact new export.** Reopen it, compare corrected text, count/inspect images and figure order, check page boundaries and filename. Report which checks succeeded and which exporter/viewer or page limits blocked. An export check cannot verify Moodle upload, receipt, approval, or grade.

## Pitfalls

- Correct source text does not establish export contents; PDF page count does not establish visual integrity.
- Correctly resolving links in a draft does not establish that images appear in the PDF/DOCX.
- Do not claim rendered-layout verification from a text-only parser.
