# AI Agent College Skills

Four agent-created skills for Hermes, plus separate OpenClaw adaptations, grew out of my Cork College of FET assignments. Classmates might find them useful, but they reflect my briefs and how I work. This repository is not assessed work; assignment AI-use rules apply when using the skills on coursework, not when developing the repository. Check your own brief and instructor directions.

### A dedicated agent profile is strongly recommended if you plan to use your choice of agent for other purposes

## Included skills

- [`academic-assignment-support`](skills/academic-assignment-support/SKILL.md) helps review briefs and drafts while keeping assessed writing with the learner. It includes a course-specific rules reference and an AI-use disclosure template.
- [`completed-assignment-cleanup`](skills/completed-assignment-cleanup/SKILL.md) helps archive old drafts without changing the submitted file or original evidence.
- [`assessment-evidence-audit`](skills/assessment-evidence-audit/SKILL.md) maps brief requirements to visible evidence in the current report and flags gaps without inventing proof.
- [`assignment-export-verification`](skills/assignment-export-verification/SKILL.md) compares an editable report with its PDF/DOCX export and checks images and page layout.

These are copies of skills from my own Hermes setup, not official Hermes skills. [Design principles](DESIGN_PRINCIPLES.md) explains the choices behind them.

## Development approach

Hermes comes first: develop and review skills and improvements in `skills/` before adapting them for OpenClaw. OpenClaw equivalents follow once the corresponding Hermes work is ready; they are not developed in parallel by default or required to complete the Hermes phase. Existing `openclaw-skills/` copies may therefore lag behind Hermes. Deferred adaptations are tracked in [TODO.md](TODO.md). Each adaptation still needs OpenClaw-specific tool and runtime checks; a ready Hermes skill does not prove OpenClaw support.

## Hermes installation

### Manual installation

Use Hermes' GitHub installer rather than copying folders. It records each skill's source so Hermes can check for updates later. You do not need a clone, ZIP download, or third-party tap.

#### Fresh installation

1. Read the four skills linked above. [`standing-ai-use-rules.md`](skills/academic-assignment-support/references/standing-ai-use-rules.md) quotes a brief from my course and includes a clarification reported by one learner. Even if you're in the same course, check your own current brief and instructor directions.
2. Choose the target Hermes profile and check for same-named installed skills. Back up their complete directories outside the profile's skill folders and compare any local edits before replacing them. If you previously copied these skills into place, follow [Migrating old folder copies](#migrating-old-folder-copies) first.
3. Run these commands in a terminal for the default profile. For a named profile, replace each `hermes skills install` with `hermes -p NAME skills install`, using its real profile name. Review each security scan and confirm only if you accept the source and any warnings. Do not use `--force` to bypass a blocked scan. Check that each command reports `Installed:`; a cancelled prompt is not a successful installation.

   ```sh
   hermes skills install User19576/ai-agent-college-skills/skills/academic-assignment-support
   hermes skills install User19576/ai-agent-college-skills/skills/completed-assignment-cleanup
   hermes skills install User19576/ai-agent-college-skills/skills/assessment-evidence-audit
   hermes skills install User19576/ai-agent-college-skills/skills/assignment-export-verification
   ```

4. Run `hermes skills list --source hub --enabled-only` (or `hermes -p NAME skills list --source hub --enabled-only`). Confirm all four names and inspect their installed directories for `SKILL.md` and any source `references/` or `templates/` folders. Start a new chat in that profile and check `/skills` to confirm discovery there.

This installs only the four skills. It does not change `SOUL.md`, `memories/USER.md`, or `memories/MEMORY.md`. If you want to consider separate profile changes, see the optional [coursework profile suggestions](installation/PROFILE_SUGGESTIONS.md). They are not intended to copy my personal details into your profile. See the [Hermes skills guide](https://hermes-agent.nousresearch.com/docs/guides/work-with-skills) for more on loading skills.

#### Migrating old folder copies

Skills copied from a ZIP or clone do not have a registered update source. To migrate those copies:

1. Locate the four college skill directories in the target profile. Compare their contents with this repository, including any `references/` and `templates/` folders, and identify local edits you want to keep.
2. Move only those old copied directories to a unique backup location outside all configured skill folders. Keep the complete backups; do not delete them.
3. Run the four GitHub installer commands above for that same profile, then verify the installation as described in step 4. If installation fails, preserve any partial result separately before restoring the affected old directories from backup. Restoring folder copies does not register them for updates.

Keep local edits in the backup until you decide whether to reapply them. Reapplying edits makes the installed skill locally modified, so Hermes will skip it during normal updates.

### Updating Hermes skills

Both the manual commands above and the agent-assisted installer below record the GitHub source. Updates are explicit, not automatic. Back up installed skills before updating and review the check results first.

These commands check and update **all hub-installed skills in the selected profile**, including unrelated skills:

```sh
hermes skills check
hermes skills update
```

To limit the operation to one college skill, include its name:

```sh
hermes skills check academic-assignment-support
hermes skills update academic-assignment-support
```

Repeat with the other college skill names if you want to update only this collection. For a named profile, replace `NAME` with its real profile name:

```sh
hermes -p NAME skills check
hermes -p NAME skills update
```

Those commands also cover all hub-installed skills in that profile. Append a skill name to target only that skill, for example `hermes -p NAME skills update academic-assignment-support`.

Hermes skips locally edited skills by default; compare those edits with upstream rather than using `--force` as routine maintenance. Review the update result, verify the installed files, and check the skills in a new chat. See the [Hermes update lifecycle](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills#update-lifecycle).

### Install via Hermes prompt

Paste this once into Hermes. It will ask which optional [profile suggestions](installation/PROFILE_SUGGESTIONS.md) you want, gather only the identifiers you choose to save, and show one combined plan. After typed approval, it will install, apply approved profile changes, and verify them. You can choose skills only. After verification, it will separately offer an optional third-party skill; that offer is not part of the approved installation.

```text
Install academic-assignment-support, completed-assignment-cleanup, assessment-evidence-audit, and assignment-export-verification directly from https://github.com/User19576/hermes-agent-college-skills into my Hermes profile; no clone. Read installation/FOR_HERMES.md and installation/PROFILE_SUGGESTIONS.md there. In this setup, use clarify (or equivalent) to ask which optional SOUL.md, USER.md, MEMORY.md changes I want; offer skills-only. Ask exact identifiers only if I choose to save them; infer none, write no placeholders. If questions time out or the tool is unavailable, ask in chat and wait; never assume skills-only. Preview one exact plan and the observed LOW scan warning. Wait for the guide's typed approval before any installation or profile write. Then complete and verify all approved changes without a second installation request. Only after verification, explain the optional third-party skill from juliusbrussee/caveman, link its source, give its install command, and ask whether I want it. Do not install it under this approval.
```

## OpenClaw installation

Use the separate [`openclaw-skills/`](openclaw-skills/) copies, **not** the Hermes `skills/` folders. They name OpenClaw's tools; see the [docs-and-source tool map](installation/OPENCLAW_TOOLS.md). OpenClaw [installs local skill directories](https://docs.openclaw.ai/cli/skills) into an agent workspace by default, not all agents' shared skills.

### Manual installation

1. Get the repository from GitHub with **Code → Download ZIP** and extract it, or run `git clone https://github.com/User19576/hermes-agent-college-skills.git`. Open a terminal in the extracted repository root.
2. Read the four `SKILL.md` files under [`openclaw-skills/`](openclaw-skills/) and the academic skill's [rules reference](openclaw-skills/academic-assignment-support/references/standing-ai-use-rules.md). The reference describes one learner's brief and reported clarification, not your own course rules. Choose the target OpenClaw agent and check whether it has same-named skills; back those up before replacing anything.
3. From the repository root, run the commands below for the default agent. For another agent, add `--agent ID` to **each** command with its real agent ID. Do not use `--global` unless you deliberately want all agents using that OpenClaw state to see the skills.

   ```sh
   openclaw skills install ./openclaw-skills/academic-assignment-support
   openclaw skills install ./openclaw-skills/completed-assignment-cleanup
   openclaw skills install ./openclaw-skills/assessment-evidence-audit
   openclaw skills install ./openclaw-skills/assignment-export-verification
   ```

4. Run `openclaw skills list` and `openclaw skills check` for the default agent, or add `--agent ID` to both for the selected other agent. Confirm all four skills are visible and the academic skill's `references/` and `templates/` were copied. Start a new session if its skill list has not refreshed.

These copies keep the coursework boundaries but use OpenClaw tool names. `read` does not parse binary DOCX; PDF page limits, converter availability, tool policy, and actual rendering still need checking. No OpenClaw runtime was available here to test them end to end. This manual route changes no identity or memory files.

### Install via OpenClaw prompt

For an approval-gated agent install, use [the OpenClaw guide](installation/FOR_OPENCLAW.md). It asks which optional `SOUL.md`, `USER.md`, and `MEMORY.md` additions you want before showing one combined, file-by-file plan. You can choose skills only. OpenClaw uses workspace-root files; on a supported multi-user Gateway, personal `USER.md` has a separate authenticated destination. The guide does not change Hermes profile files:

```text
Install the four OpenClaw-native college skills from openclaw-skills/ in https://github.com/User19576/hermes-agent-college-skills for my selected OpenClaw agent. Read installation/FOR_OPENCLAW.md and installation/OPENCLAW_TOOLS.md there first. Identify my agent, workspace, and whether its USER.md is shared or personal. Ask which optional SOUL.md, USER.md, and MEMORY.md additions I want; offer skills-only. Ask exact identifiers only if I choose to save them, and never write placeholders or someone else's details. Show one combined plan with exact target diffs or no change; wait for APPROVE OPENCLAW COLLEGE SKILLS INSTALL before cloning, installing, or changing any profile file. Then verify all approved changes without treating the approval as consent for anything else.
```

## Related skills — for Hermes

Hermes normally bundles these five skills, so you usually don't need to install them. A profile can disable or omit them; check `hermes skills list --source builtin --enabled-only` if one is missing. `humanizer` started as a third-party skill and was ported into Hermes.

- Nous Research: [`pdf`](https://github.com/NousResearch/hermes-agent/tree/main/skills/productivity/pdf) for briefs and exports; [`docx`](https://github.com/NousResearch/hermes-agent/tree/main/skills/productivity/docx) for Word reports.
- Co-authored: [`obsidian`](https://github.com/NousResearch/hermes-agent/tree/main/skills/note-taking/obsidian) for the assignment tracker (Teknium and Hermes Agent); [`grounded-citations`](https://github.com/NousResearch/hermes-agent/tree/main/skills/research/grounded-citations) for source-backed research (Hermes Agent and Teknium).
- Third-party origin: [`humanizer`](https://github.com/blader/humanizer) for wording edits. It is [listed on skills.sh](https://www.skills.sh/blader/humanizer/humanizer) and linked here, not copied into this repository.

This list shows related tools, not a count of past skill uses. The skills in this repository use the [MIT License](LICENSE). The related skills above keep their own licenses.

### Optional skill not included with standard Hermes installs

[`caveman`](https://github.com/juliusbrussee/caveman/blob/main/skills/caveman/SKILL.md) from [`juliusbrussee/caveman`](https://github.com/juliusbrussee/caveman) offers terse replies while retaining technical detail. It is not one of this repository's four skills and is not part of the install above. Inspect the upstream skill before choosing to install it. For the default profile, run:

```sh
hermes skills install juliusbrussee/caveman/skills/caveman
```

For a named profile, run `hermes -p NAME skills install juliusbrussee/caveman/skills/caveman` with its real profile name. Review the security scan and any existing same-named skill before confirming. Start a new chat in that profile and check `/skills` or `hermes skills list --enabled-only` (add `-p NAME` for a named profile). Installation does not enable a standing reply style by itself; request the style separately if wanted.
