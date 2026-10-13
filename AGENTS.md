# Hermes College Skills

This directory is the working copy of `User19576/hermes-agent-college-skills`. `IDEA.md` records the original plan; `README.md` and `DESIGN_PRINCIPLES.md` describe the skills and their scope.

## Current state

- `skills/academic-assignment-support/` contains `SKILL.md`, a course-specific rules reference, and a disclosure template. `skills/completed-assignment-cleanup/`, `skills/assessment-evidence-audit/`, and `skills/assignment-export-verification/` each contain `SKILL.md`.
- `openclaw-skills/` contains four OpenClaw-specific skill copies, with the academic rules reference and disclosure template kept inside its skill directory. They use OpenClaw tool names; neither set is a substitute for runtime verification of coursework workflows.
- The root README links related bundled Hermes and third-party skills without vendoring them. These included skills are course-specific; do not present them as general academic policy.
- The root README documents Hermes installation and a workspace-scoped OpenClaw installation route using `openclaw-skills/`, not `skills/`. `installation/FOR_HERMES.md` holds the approval-gated Hermes procedure; it is not a local-clone workflow. `installation/FOR_OPENCLAW.md` covers approval-gated local-directory installs after a reviewed checkout, with separately consented OpenClaw workspace SOUL/USER/MEMORY additions and multi-user personal USER targeting. `installation/OPENCLAW_TOOLS.md` cites native tool documentation and source code. `installation/PROFILE_SUGGESTIONS.md` gives optional Hermes SOUL/USER/MEMORY source examples without publishing the author's identifiers; OpenClaw-specific destinations and wording live in its own guide. `LICENSE` contains the MIT terms.
- No manifests, lockfiles, CI workflows, tests, or lint configuration are present. No setup, build, test, or lint commands are defined.

## Repository

- Public GitHub repository: `https://github.com/User19576/hermes-agent-college-skills`. Check the remote branch before claiming a change was pushed.
- Before changing any existing project file, copy its current bytes to a unique `archive/<timestamp>/<repo-relative-path>` location. Preserve the relative path and never overwrite an earlier snapshot. Compare source and snapshot hashes before editing. New files have no prior version to save. Root `.gitignore` excludes `/archive/`; do not stage or publish snapshots.

## Scope

- This skill-collection project is not an assignment; college assignment AI-use rules do not apply to work in this folder. Apply assessment rules separately when using a skill on an actual assignment.
- Update this file when real skill layout, documentation, or verified commands exist; record observed conventions rather than predictions.
