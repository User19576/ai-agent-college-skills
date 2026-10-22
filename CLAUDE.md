# CLAUDE.md

File gives Claude Code (claude.ai/code) guidance for code in this repo.

## Commands

No build, lint, or test commands. No manifests, lockfiles, CI, or test config; `AGENTS.md` confirms none defined. Don't invent them. Verify by reading files and checking Markdown and install commands against docs they reference.

- `tests/` and `archive/` gitignored. `tests/` holds Hermes session exports (JSON), not test suite. Don't commit or quote from them.
- `/archive/` = snapshot location (see below). Never stage it.

## Project rules (from AGENTS.md)

- **Archive before editing.** Before changing existing project file, copy current bytes to `archive/<timestamp>/<repo-relative-path>`. Never overwrite earlier snapshot. Compare source and snapshot hashes before editing. New files need no snapshot.
- **Hermes first.** Develop and review skills in `skills/`. Adapt to `openclaw-skills/` only once Hermes work ready. Track deferred OpenClaw work in `TODO.md`. Don't develop both trees in parallel by default.
- **Preserve settled behaviour when adapting.** OpenClaw copies use OpenClaw tool names, need own runtime checks. Ready Hermes skill ≠ OpenClaw support.
- **Check the remote before claiming a push.** Remote: `https://github.com/User19576/hermes-agent-college-skills`.
- **Update `AGENTS.md`** when real skill layout, docs, or verified commands change. Record observed conventions, not predictions.

## Architecture

Repo = docs-and-skills collection, not program. Each skill = Markdown `SKILL.md` with YAML frontmatter (`name`, `description`, `version`, `author`, `license`, `metadata.hermes`), optionally `references/` and `templates/`.

- **Two parallel trees, one behaviour.** `skills/` = Hermes source. `openclaw-skills/` = OpenClaw adaptation, lags behind, uses OpenClaw tool names. Both share same four skills: `academic-assignment-support` (includes `references/standing-ai-use-rules.md` and `templates/AI-DISCLAIMER.md`), `completed-assignment-cleanup`, `assessment-evidence-audit`, `assignment-export-verification`.
- **Install docs are part of the product.** `README.md` documents install routes. `installation/FOR_HERMES.md` and `installation/FOR_OPENCLAW.md` = approval-gated agent procedures, not local-clone workflows. `installation/OPENCLAW_TOOLS.md` maps tools to OpenClaw docs and source. `installation/PROFILE_SUGGESTIONS.md` holds optional Hermes SOUL/USER/MEMORY examples. Changing one usually needs matching changes in others.
- **Design rules live in `DESIGN_PRINCIPLES.md`.** Main ones: start from current brief, keep learner's work theirs, separate claims from evidence, check actual deliverable, preserve record, disclose actual assistance.

## Scope and publishing

- Repo not assessed work. Assignment AI-use rules apply when skill used on actual coursework, not when developing it.
- `standing-ai-use-rules.md` reference quotes one learner's brief and reported clarification. Don't present as general academic policy.
- Don't publish personal identifiers, machine paths, live assignment status, or one-off course exceptions as general guidance (`DESIGN_PRINCIPLES.md`, `installation/PROFILE_SUGGESTIONS.md`).
- Bundled third-party skills (`humanizer`, `caveman`, Nous Research skills) linked, not vendored. Keep that way.