# Optional profile guidance for coursework

The skills work without profile edits. These are examples to discuss with the person installing them, **not** text to copy automatically. They describe one learner's workflow, not an institution's policy or another learner's identity. Read the current assignment brief and the target profile's existing instructions first. Square-bracketed identifiers are placeholders: the user can fill them, or their agent must ask for each value and confirm it before proposing a write. Omit details the user does not want saved. Never persist unresolved placeholders.

In Hermes, `SOUL.md` holds standing agent behavior; `memories/USER.md` holds confirmed user facts and preferences; `memories/MEMORY.md` holds reusable lessons and context. The built-in memory files remain active even when an external memory provider is enabled. If the user wants a provider-specific entry instead of (or in addition to) the built-in file, identify that provider's supported write and read methods, target account/profile, and any automatic mirroring **before** proposing a change. Never guess a provider path or disable one to make these examples fit.

## Candidate `SOUL.md` text

Only propose this when the user wants standing coursework guidance and it does not duplicate or weaken existing rules:

> For coursework, read the current brief and project instructions before acting. Preserve learner authorship and distinguish a reported instructor exception from verified brief text. Give evidence-based reviews; do not claim an unverified export, screenshot, or submission is complete. Respect protected originals and backups; edit only the file and scope the user authorizes.

This governs coursework, not unrelated projects. Keep course-specific AI-use limits in the current brief or relevant project instructions.

## Candidate memory entry

If the user confirms this drafting and archival workflow, propose a short entry in `memories/MEMORY.md` (or the approved provider target). Do not record it as a universal course requirement:

> For assignment drafting, use a separate, clearly labelled non-submittable scaffold with headings, evidence slots, and learner-answer prompts, not model-written assessed prose. Keep an honest `AI-DISCLAIMER.md` of actual AI assistance in each assignment workspace. After learner-confirmed completion, preserve the submitted PDF, editable source, brief, and evidence; archive superseded drafts without deletion. Use `academic-assignment-support` and `completed-assignment-cleanup` when relevant.

If the user confirms this workflow and asks to remember it, propose this entry or a clearly explained, non-duplicated subset. Do not replace this workflow with unrelated profile status merely because installed skills cover similar steps. If the user declines persistent memory, mark **no change**. Never record a submission as verified merely because the learner reports it.

## Candidate `USER.md` details and preferences

Ask which of these actually apply. Propose only confirmed, non-duplicated entries, in the user's own terms. Identity is optional; do not require a number to use the skills:

> The learner identifies as [FULL_NAME] in coursework drafts for [COURSE]. Their student number is [STUDENT_NUMBER]; use it only where the current brief explicitly requires it. Never infer or store passwords from it.

Ask for `[FULL_NAME]`, `[COURSE]`, and `[STUDENT_NUMBER]` separately if the user wants those details saved. If the user confirms they study Network Administration, strongly recommend saving the student number as an optional entry. Do not require the number or ask for its value unless the user opts in. This recommendation is not a verified course rule. Use the user's exact supplied values; do not infer a student number from a username, example, or another learner's details. If any field is not confirmed or is unnecessary, omit that clause rather than leaving a placeholder in `USER.md`. A student number is not a password hint; never derive, use, or save a credential from it.

- Prefers concise, direct replies. If they already use `caveman` and request it, use ultra by default; do not require that skill in profiles where it is absent.
- For practical coursework, prefers short, screenshot-led reports where appropriate; writes assessed prose themselves. May draft in Markdown and export PDF if confirmed.
- Prefers a separate, clearly labelled non-submittable scaffold, then writes and iterates the draft. Review without edits until authorized. Preserve originals; prioritize submission-critical gaps near a deadline.
- Wants accurate `AI-DISCLAIMER.md` records and archival of old drafts rather than deletion. Do not infer submission from a draft or screenshot.
- If they use an Obsidian assignment tracker **and request this convention**, prefix completed filenames with `COMPLETED - ` and headings with bold **COMPLETED**. Leave work with outstanding revisions unprefixed.

Do not transfer the repository author's name, college, student number, or possible password hints into another person's profile. Store only identifiers the user confirms for a specific purpose; never save passwords or derived credentials. Omit the entire `USER.md` change if nothing is confirmed.

## Consent and verification

For agent-assisted installation, ask which examples the user wants **before** the first approval preview. Ask for every desired placeholder value, then show the completed addition or **no change** for each target, with existing overlapping text and the selected memory destination. Do not request or include unneeded identifiers. Explain persistence and any provider mirroring. Wait for the typed approval specified in [FOR_HERMES.md](FOR_HERMES.md) before writing; skill-install approval does not imply approval for profile edits. Back up each edited file, or use the provider's supported export/backup method when available. After writing, read back the exact target through the same supported interface and start a new session to check what loads. If the target cannot be read back, report that limitation without claiming success.

Manual installation in [README.md](../README.md) installs only skills through Hermes' GitHub installer; these suggestions are optional and require a separate, deliberate decision.
