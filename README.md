# AI Agent College Skills

Four agent-created skills for Hermes, plus separate OpenClaw adaptations, grew out of my Cork College of FET assignments. Classmates might find them useful, but they reflect my briefs and how I work. This repository is not assessed work; assignment AI-use rules apply when using the skills on coursework, not when developing the repository. Check your own brief and instructor directions.

### A dedicated agent profile is strongly recommended if you plan to use your choice of agent for other purposes

## Included skills

- [`academic-assignment-support`](skills/academic-assignment-support/SKILL.md) helps review briefs and drafts while keeping assessed writing with the learner. It includes a course-specific rules reference and an AI-use disclosure template.
- [`completed-assignment-cleanup`](skills/completed-assignment-cleanup/SKILL.md) helps archive old drafts without changing the submitted file or original evidence.
- [`assessment-evidence-audit`](skills/assessment-evidence-audit/SKILL.md) maps brief requirements to visible evidence in the current report and flags gaps without inventing proof. Its [filesystem and share evidence reference](skills/assessment-evidence-audit/references/filesystem-and-share-evidence.md) distinguishes command scope, permission modes, recursive changes, and mount evidence.
- [`assignment-export-verification`](skills/assignment-export-verification/SKILL.md) compares an editable report with its PDF/DOCX export and checks images and page layout.

These are copies of skills from my own Hermes setup, not official Hermes skills. [Design principles](DESIGN_PRINCIPLES.md) explains the choices behind them.

## Development approach

Hermes comes first: develop and review skills and improvements in `skills/` before adapting them for OpenClaw. OpenClaw equivalents follow once the corresponding Hermes work is ready; they are not developed in parallel by default or required to complete the Hermes phase. Existing `openclaw-skills/` copies may therefore lag behind Hermes. Deferred adaptations are tracked in [TODO.md](TODO.md). Each adaptation still needs OpenClaw-specific tool and runtime checks; a ready Hermes skill does not prove OpenClaw support.

The Hermes guidance covers bounded revision feedback, durable research-review notes, reversible evidence organisation, and scoped source/export checks. Markdown/PDF text extraction, HTML image paths, PDF image placements, and exporter-specific pagination are inspection methods, not blanket compatibility claims. The documented procedures still need exercising on the exact documents and available tools before reporting a successful export, filesystem/share test, or installation.

## Hermes installation

### Manual installation

1. Get the files from GitHub. Use **Code → Download ZIP** and extract it, or run `git clone https://github.com/User19576/hermes-agent-college-skills.git`.
2. Read the four skills linked above. [`standing-ai-use-rules.md`](skills/academic-assignment-support/references/standing-ai-use-rules.md) quotes a brief from my course and includes a clarification reported by one learner. Even if you're in the same course, check your own current brief and instructor directions.
3. Open your Hermes skills folder: `%LOCALAPPDATA%\hermes\skills` on Windows or `~/.hermes/skills` on macOS/Linux. If you use a named profile, find its own `profiles/<name>/skills` folder under your Hermes home. If `HERMES_HOME` is set to the active profile, use its `skills` folder. Create the folder if it doesn't exist.
4. Copy `academic-assignment-support/`, `completed-assignment-cleanup/`, `assessment-evidence-audit/`, and `assignment-export-verification/` from this repository's `skills/` into your Hermes `skills/`. Keep `SKILL.md` and any `references/` or `templates/` folders in place. If any skill already exists, back it up and compare the copies before replacing it.
5. Start a new chat in that profile and type `/skills`. You should see all four names. You can also run `hermes skills list --enabled-only` (or `hermes -p NAME skills list --enabled-only` for a named profile). If a skill is missing, check that `SKILL.md` sits directly inside its folder.

This installs only the four skills. It does not change `SOUL.md`, `memories/USER.md`, or `memories/MEMORY.md`. If you want to consider separate profile changes, see the optional [coursework profile suggestions](installation/PROFILE_SUGGESTIONS.md). They are not intended to copy my personal details into your profile. See the [Hermes skills guide](https://hermes-agent.nousresearch.com/docs/guides/work-with-skills) for more on loading skills.

### Install via Hermes prompt

Paste this once into Hermes. It will ask which optional [profile suggestions](installation/PROFILE_SUGGESTIONS.md) you want, gather only the identifiers you choose to save, and show one combined plan. After typed approval, it will install, apply approved profile changes, and verify them. You can choose skills only. After verification, it links the optional [Caveman skills](#optional-caveman-skills) for you to explore and install manually using the upstream instructions. Caveman installation is not part of this prompt or approval.

```text
Install academic-assignment-support, completed-assignment-cleanup, assessment-evidence-audit, and assignment-export-verification directly from https://github.com/User19576/hermes-agent-college-skills into my Hermes profile; no clone. Read installation/FOR_HERMES.md and installation/PROFILE_SUGGESTIONS.md there. In this setup, use clarify (or equivalent) to ask which optional SOUL.md, USER.md, MEMORY.md changes I want; offer skills-only. Ask exact identifiers only if I choose to save them; infer none, write no placeholders. If questions time out or the tool is unavailable, ask in chat and wait; never assume skills-only. Preview one exact plan and the observed LOW scan warning. Wait for the guide's typed approval before any installation or profile write. Then complete and verify all approved changes without a second installation request. Only after verification, briefly recommend optional Caveman skills by linking https://github.com/JuliusBrussee/caveman and its current installation instructions at https://github.com/JuliusBrussee/caveman/blob/main/INSTALL.md. Direct me to the manual skills-only route for my chosen agent, not Caveman services or runtime setup. Do not offer to install Caveman, ask installation-selection questions, or supply a Caveman installation prompt; this workflow ends with the recommendation and links.
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

### Optional Caveman skills

The [Caveman repository](https://github.com/JuliusBrussee/caveman) includes skills for shorter replies and coding workflows. They are third-party skills, not included with standard Hermes installs or this repository's four college skills. You do not need them to use the college skills, but they are recommended for reduced costs and shorter answers.

For reply style, [`caveman`](https://github.com/JuliusBrussee/caveman/blob/main/skills/caveman/SKILL.md) aims to remove filler while keeping technical detail. [`ultracave`](https://github.com/JuliusBrussee/caveman/blob/main/skills/ultracave/SKILL.md) uses shorter fragments; [`megacave`](https://github.com/JuliusBrussee/caveman/blob/main/skills/megacave/SKILL.md) uses Classical Chinese. These are separate skills: installing `caveman` alone does not install the other modes. Workflow skills such as [`investigate-first`](https://github.com/JuliusBrussee/caveman/blob/main/skills/investigate-first/SKILL.md) and [`verify-and-stop`](https://github.com/JuliusBrussee/caveman/blob/main/skills/verify-and-stop/SKILL.md) guide diagnosis and focused verification.

This recommendation is for **skills only**, selected from the current upstream source without a required connection to Caveman Cloud services. I personally don't recommend using said Caveman services, at least not on the free plan. The skills still use your agent's model and tools; a hosted model is not offline. Some skills need scripts, model APIs, a local CLI, or host-specific features. Skills requiring a Caveman service are omitted from the offer, without suggestions to install them later.

#### Manual installation

Visit the [Caveman repository](https://github.com/JuliusBrussee/caveman) and follow its current [installation instructions](https://github.com/JuliusBrussee/caveman/blob/main/INSTALL.md). Choose the skills-only route and the instructions for your agent, rather than the full runtime or service setup. This repository does not provide a prompt for Hermes or another agent to install Caveman for you.