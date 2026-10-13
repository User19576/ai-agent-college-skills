---
name: academic-assignment-support
description: Review coursework without writing assessed work for the learner.
---

# Academic Assignment Support (OpenClaw)

Use for assessed reports, practical demonstrations, and coursework. This repository of skills is not itself assessed work. The original learner's rules in `references/standing-ai-use-rules.md` are course context, not policy for a new learner; never transfer their instructor clarification to another assignment.

## Available tools and limits

- Use OpenClaw `ls` to inventory folders and `read` for text and images. For a recursive file search, use `exec` with an available local search command only when permitted; `ls` is a directory listing, not a recursive glob search.
- Use OpenClaw `pdf` to analyze a PDF brief. Its page and size budgets can return partial results; check the result and inspect pages containing diagrams. `read` does not extract binary documents such as DOCX. Use an available document parser/converter through approved `exec` for DOCX, or report the blocker.
- Use `view_image` for local screenshot or rendered-page inspection. When text is too small, make a non-destructive crop or higher-resolution render using an available approved tool, then inspect that image. Do not invent a crop option on `view_image`.
- Use `web_search` and `web_fetch` for primary research sources if available; `web_search` may require a configured provider. Check the actual tool list and policy before assuming a capability is enabled.
- Use `write`, `edit`, or `apply_patch` only for authorized files; use `exec` for approved shell operations and hashes. Tool permissions and workspace boundaries still apply.

## Procedure

1. **Discover constraints.** Read the active workspace instructions (`AGENTS.md` and other current project rules), assignment brief, and current draft. Inventory the evidence and related files. For PDF briefs, check whether `pdf` processed every relevant page; inspect embedded diagrams or screenshots rather than relying solely on extracted text. Identify deliverable format, evidence, allowed AI uses, and submission requirements. Treat any learner-reported exception as reported, not verified brief text; update dependent checks only within its stated scope.
2. **Preserve authorship.** Offer feedback, source notes, evidence checks, grammar/spelling review, and separate non-submittable scaffolds when permitted. Do not compose a final report, reflective section, or substantial assessed prose for the learner. Research notes must remain distinct from submission text; prefer original vendors, standards bodies, or official documentation and cite checked sources.
3. **Review actual work.** Read the current draft and inspect every relevant linked screenshot; names may stay constant while files change. For evidence-only requests, distinguish loose files from images embedded in the report. Identify observed issues by section or page. Check host application and VM identity, exact settings and targets, packet loss, route hops, and current evidence rather than treating a technically working alternative as proof of literal brief compliance. Accept learner-declared mock placeholders or intentionally body-only scope instead of repeatedly flagging them.
4. **Create support files only on request.** Use a separate, clearly labelled non-submittable scaffold with brief-ordered headings, evidence slots, and learner-answer prompts. Never insert invented screenshots, captions, or assessed explanations. Resolve links before claiming the scaffold works. When authorized to edit a working copy, preserve learner prose, back up protected originals, and change only the named scope.
5. **Record real assistance.** In an assignment workspace, maintain an accurate `AI-DISCLAIMER.md` when permitted by the current brief. Read the existing record first; use `templates/AI-DISCLAIMER.md` as a guide, not an unfilled deliverable. Record actual review, research, created files, and edits. Do not claim learner approval, submission, or an instructor's permission without evidence. Do not automatically edit workspace `USER.md` or `MEMORY.md` to transfer the original learner's rules.
6. **Verify and report.** Reopen changed artifacts and their final export where relevant. State what was read or rendered and which evidence or policy checks remain unverified. A filename, PDF package check, screenshot, or learner report alone is not a submission receipt.

## Pitfalls

- A PDF text layer can omit values shown in diagrams. `pdf` may analyze only a configured page budget; a partial result is not a full brief check.
- A successful connectivity test does not establish route hops, absence of packet loss, or brief compliance. A snapshot cannot restore work unless one exists.
- An approved document edit is not permission to change protected backups or overwrite a submitted artifact.
- Do not save a student number unless the learner chooses that scope; never derive or store a password from it.
