# College-skill review — implementation record

Reviewed: 2026-10-20. Repository HEAD: `fe65afd464504de0eed86a23506dd9d6a6afe982`.

The reviewed additions below are now integrated selectively into the repository's working documentation. Checked boxes mean source guidance was added, not that the described coursework workflows were exercised. Stronger repository safeguards remain in place. This is the implementation record for this review, not an unresolved backlog; replace it after the next fresh comparison rather than carrying items forward automatically.

## Boundaries

- Keep `/SUGGESTIONS.md` Git-ignored. Replace after every fresh review; never retain stale items automatically.
- Hermes first. OpenClaw adaptation remains separate follow-up in `TODO.md`; no runtime compatibility claim.
- Merge rules selectively. Never replace repository skills wholesale with installed copies.
- Preserve stronger repository safeguards: cross-learner policy scope; uncertain tutor corrections; stage-appropriate feedback; optional explanations; exact edit targets; prompt-only changes; command-label scope; actual chronology; backups; explicit export authorization.
- Preserve export safeguards: fresh renders and pixel hashes; viewer-discrepancy investigation; completed repairs or explicit blockers; exact exporter identification.
- Exclude private memory, assignment paths, identifiers, credentials, one-off exceptions from public additions.
- Source review only. No coursework export, installation, filesystem/share test, or OpenClaw runtime exercised.

## Academic assignment support

Source: installed `academic-assignment-support/SKILL.md`.
Target: `skills/academic-assignment-support/SKILL.md`.

### 01. Bound revision feedback

- [x] Reread small revisions. Check whether original issue resolves or merely changes wording. Give bounded follow-up, not another full audit.
- State command intent and evidence limits together; avoid moving requirements across replies.
- Verify: passage-only revision receives passage-specific feedback unless new evidence warrants wider review.

### 02. Retire stale evidence findings

- [x] Track learner-planned evidence as pending. Recheck at final evidence review; do not repeatedly present known absence as new defect.
- When replacement evidence resolves a finding, reconcile authorized checklist, scaffold, and project instructions. Without edit permission, identify stale notes instead.
- Verify: resolved findings close; pending requirements remain visible, never labelled complete without evidence.

### 03. Respect research-review stages

- [x] When requested before DOCX creation, save short, labelled research notes in assignment root unless another location is specified.
- Chat text or expiring scratch files do not satisfy durable-artifact requests. Wait for learner review before deferred DOCX baseline; default to same root.
- Keep notes distinct from assessed prose.
- Verify: reviewable notes exist; deferred baseline waits for review.

### 04. Separate required headings from unspecified design

- [x] Use marking-scheme headings in printed order. Do not invent font, page-design, or assessed-paragraph requirements.
- For short screenshot-led scaffolds, use brief-ordered image groups and one concise learner-answer prompt per group. Keep detailed cautions in review notes.
- Preserve no-duplicate-outline rule and bounded, learner-authorized prompt insertion.
- Verify: headings match brief; unspecified visual design remains explicitly unspecified.

### 05. Interpret cleanup markers within scope

- [x] Treat learner-defined arrow placeholders or starred cleanup notes as instructions, not assessed prose. Apply/remove only with cleanup authorization.
- Preserve protected originals and legitimate answers resembling markers. Leave missing assessed content for learner.
- Verify: only identified markers and authorized cleanup targets change.

### 06. Equalize image widths without distortion

- [x] For authorized cleanup of unlabeled groups, use `<img src="..." width="...">`; omit forced `height` to preserve aspect ratio.
- Resolve raw HTML image paths. Retain Markdown PDF sanitization caveat and extension-versus-Chromium distinction.
- Verify exact fresh export: images load, widths match intent, aspect ratios remain intact.

### 07. Distinguish diagnostic results from required invocations

- [x] Credit visible equivalent output, e.g. `ip a` instead of `ifconfig` for interface addresses. Label actual command accurately.
- Assess literal invocation separately when brief explicitly grades command used. Preserve exact configuration-value requirements.
- Verify: demonstrated result credited; outstanding literal-command requirement identified separately.

### 08. Make scan organization reversible

- [x] For authorized renaming, inspect visible question numbers before ordering; phone filenames need not match question order.
- Check destination collisions. Preserve image bytes; verify before/after hashes. Keep original-to-new path index.
- Organization does not authorize generating or correcting answers.
- Verify: hashes match; every original maps to unique destination; index explains order.

## Assessment evidence audit

### 09. Add filesystem/share evidence reference

- [x] Review installed `assessment-evidence-audit/references/filesystem-and-share-evidence.md` for public use; add as `skills/assessment-evidence-audit/references/filesystem-and-share-evidence.md`.
- Source also includes installed `assessment-evidence-audit/SKILL.md`, Procedure step 3. Add targeted pointer in repository `skills/assessment-evidence-audit/SKILL.md`, same step.
- Separate learner-reported execution, command scope, screenshot-confirmed results. Listed command alone does not prove outcomes for every object.
- Retain distinctions: `ls -ld DIRECTORY` shows directory itself; leading `d` is object type, not permission bit. Directory search differs from file execution; other controls can restrict access.
- Recursive `chmod`/`chown` concerns existing reached objects, not future inheritance. Directory-only screenshots do not verify every child's mode or owner.
- Matching local modes or contents does not independently prove NFS mount, mount source, export configuration, or remote edit.
- Request `findmnt -T PATH` only for genuine requirement or unresolved mount claim. Do not expand agreed directory-only scope into recursive evidence demands.
- Verify: reference link resolves; no private values. Apply interpretations to actual evidence before claiming coursework findings.

## Assignment export verification

Source: installed `assignment-export-verification/SKILL.md`.
Target: `skills/assignment-export-verification/SKILL.md`.

### 10. Separate version authority from other checks

- [x] For sync-only questions, check local availability and changed content without automatic full assessment audit.
- Accept explicit learner latest-copy confirmation as version authority, not independently verified remote sync, export correctness, compliance, or submission receipt.
- Verify: answer requested version question; state limits of remote-state and submission claims.

### 11. Classify corrections before repeating defects

- [x] Classify reported correction: source-fixed/export-stale; corrected in both; unresolved. Name the exact source or export still containing a defect.
- Stale PDF does not make already-fixed source defect unresolved again.
- Verify: every finding identifies source or export actually containing defect.

### 12. Account for text-extraction limits

- [x] For programmatic Markdown/PDF comparison, parse Markdown with raw HTML enabled. Extract text through HTML parser; decode entities; normalize whitespace.
- Compare with PyMuPDF `page.get_text(sort=True)`. Inspect mismatches before declaring stale export: code order, headers, footers, extraction artifacts can differ.
- Document exclusions; never strip substantive text to force equality. Text equality proves neither images nor layout.
- Preserve rendered-page inspection and existing fresh-render checks.
- Verify: stale-export finding identifies real missing/changed passage. Exercise real documents before claiming tested method.

### 13. Resolve HTML images; inspect actual placements

- [x] Resolve Markdown `![...](...)` links and raw HTML `<img src="...">` paths. Syntax changes need not change image inventory.
- Use PyMuPDF `page.get_image_info(xrefs=True)` and placement `bbox` to locate raster images and inspect displayed dimensions; visually inspect affected pages.
- Reconcile repeated placements, masks, vector content with report. Unique image objects are not visible-figure counts.
- Verify: every expected figure maps to placement or rendered content, including images between numbered groups. Filenames and raster counts alone are insufficient.

### 14. Gate pagination fixes on actual exporter

- [x] For authorized VS Code Markdown PDF repair, inspect adjacent pages. Confirm installed stylesheet defines `.page { page-break-after: always; }` before using `<div class="page"></div>` immediately before section.
- Use break only when observed heading/introduction/code/evidence grouping improves. Re-export through intended route; inspect exact resulting PDF.
- Preserve edit authorization, exact-target backups, repair completion, and alternative-route safeguards. Direct Chromium output does not certify extension output.
- Verify: affected pages improve; no new split/clipping; report identifies exporter producing inspected artifact.

## No addition warranted

- `completed-assignment-cleanup/SKILL.md`: same text after line-ending normalization; byte differences only.
- `academic-assignment-support/templates/AI-DISCLAIMER.md`: same text after line-ending normalization; byte differences only.
- Keep repository standing AI-use reference: stronger cross-learner scoping, public-safe source description. Installed counterpart is not upgrade.
- No new sibling skill needed. Extend existing skills; add only focused filesystem/share reference.

## Implementation verification and remaining limits

- The user authorised documentation integration. Three Hermes skills were updated selectively; one public-safe filesystem/share reference was added. README and AGENTS inventories and the deferred OpenClaw work in TODO were updated.
- Pre-edit snapshots: `archive/20261020T114118.312187Z-suggestions-update/`. All 25 original snapshot hashes verified before editing; protected and out-of-scope files remain unchanged.
- Static checks pass: all 14 additions are represented; skill frontmatter and heading structure unchanged; stronger repository safeguards preserved; all 32 relative Markdown links resolve; `git diff --check` passes. The new reference and added lines were reviewed for private data.
- `/SUGGESTIONS.md` and the archive remain ignored. The user's pre-existing `.gitignore` change was preserved without further edits.
- No runtime workflow was exercised. PyMuPDF is unavailable in the checked Python environment. Real-document extraction, rendering/export, filesystem/share checks, installation, and OpenClaw runtime behaviour remain unverified. The per-item verification bullets above describe future workflow checks, not completed runtime tests.
- Installed academic skills, OpenClaw copies, the standing policy reference, disclosure template, and completed-assignment cleanup skill were not changed. No staging, commit, push, or merge was performed.
