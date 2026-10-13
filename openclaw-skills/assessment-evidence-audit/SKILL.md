---
name: assessment-evidence-audit
description: Audit visible report evidence against the current brief.
---

# Assessment Evidence Audit (OpenClaw)

Review the actual report against its brief; do not change assessed work or invent proof. Check `academic-assignment-support` if installed for authorship and AI-use boundaries, or read the current brief and workspace rules directly.

## Procedure

1. **Establish scope.** Use OpenClaw `ls` to find the brief, current draft, evidence folder, and deliverable; `read` handles text and image files. Use OpenClaw `pdf` for a PDF brief or report. Its configured page budget can omit pages, so verify coverage and report truncation. For DOCX use a locally available approved parser/converter via `exec`; `read` does not extract binary DOCX. Read project rules. Treat learner-reported instructor exceptions as reported unless written instructions verify them.
2. **Inspect current evidence.** Inventory every image embedded in the report (including unnumbered images) separately from loose screenshot files. Resolve Markdown image paths relative to the report. Use `view_image` to inspect screenshots, including host app title and VM tab as well as guest output. For tiny fields, generate a non-destructive high-resolution render or crop using an approved available image tool through `exec`, then inspect it with `view_image`. Do not infer appearance, order, or displayed dimensions from image filenames or loose files. If the PDF or DOCX cannot be rendered, mark visual checks unverified.
3. **Map each requirement.** For each brief step record required proof, report section/page and image, visible result, and status (`shown`, `missing`, `conflicts`, `not checkable`). Check literal values, settings, targets, addresses, packet loss, evidence order, labels, and report image-size limits. Distinguish reachability (`ping`) from route hops, and configured values from actual execution. A technically working alternative does not prove a literal requirement.
4. **Report gaps.** Cite the current brief requirement and the observed report section/page or screenshot. Say what learner evidence or correction would resolve each gap. Do not fabricate a screenshot, alter original evidence, or write final assessed prose. Do not repeatedly flag an accepted exception without new evidence.
5. **Verify claims.** Reopen linked screenshots even if the filenames have not changed. Recount images and checked brief steps against the current report. State exactly which content and layout properties were observed and which are unverified; no file inventory proves upload, receipt, approval, or grade.

## Pitfalls

- PDF text extraction can miss values in embedded diagrams; inspect rendered images as needed.
- Pixel dimensions do not establish centimetre limits in the submitted document.
- A working ping can still show packet loss or a different target.
