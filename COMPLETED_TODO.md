# Completed to-dos

## Optional SOUL, MEMORY and USER guidance

- Offer optional `SOUL.md`, `MEMORY.md` (or an approved memory provider), and `USER.md` examples. Let the user choose which entries to save; ask for and confirm identifiers before previewing completed text. Never write unconfirmed details, raw placeholders, or another learner's identifiers.
- Provide scoped `SOUL.md` guidance: read the current coursework brief first, preserve learner authorship, distinguish reported exceptions from verified instructions, review from evidence, and protect originals.
- Provide a `MEMORY.md` example for non-submittable drafting scaffolds, accurate `AI-DISCLAIMER.md` records, and preservation of completed assignment sources and evidence.
- Provide optional `USER.md` preference examples for concise feedback, learner-written assessed prose, authorized edits, accurate AI-use records, and Obsidian completion markers.

Implemented in [optional profile guidance](installation/PROFILE_SUGGESTIONS.md) and [the approval-gated installation guide](installation/FOR_HERMES.md). The optional identity example retains `[FULL_NAME]` and uses `[COURSE]`. For a confirmed Network Administration learner, the agent strongly recommends but never requires saving `[STUDENT_NUMBER]`; use in coursework still depends on the current brief.

## Post-install optional skill guidance

- Name the optional `caveman` source as `juliusbrussee/caveman` in the installation prompt and instructions, rather than leaving its origin ambiguous.
- After installing and verifying the four college skills, tell the user about additional skills not bundled with standard Hermes installs. Explain their purpose, provide an install option and exact command, and do not treat the original install approval as consent for another skill.
- Link the third-party `caveman` skill and its installation command.

Implemented in [README.md](README.md) and [the agent installation guide](installation/FOR_HERMES.md). The optional skill is [`juliusbrussee/caveman/skills/caveman`](https://github.com/juliusbrussee/caveman/blob/main/skills/caveman/SKILL.md); install it separately with `hermes skills install juliusbrussee/caveman/skills/caveman` if the user chooses it.

## OpenClaw installation route

- Added workspace-scoped manual and approval-gated OpenClaw installation instructions in [README.md](README.md) and [the OpenClaw guide](installation/FOR_OPENCLAW.md). The route now installs separate [OpenClaw-native copies](openclaw-skills/academic-assignment-support/SKILL.md), with tool names checked against [OpenClaw docs and source](installation/OPENCLAW_TOOLS.md). The earlier direct-Hermes-copy route is superseded. No OpenClaw runtime was available for an end-to-end check.
- Considered OpenCode, Pi, Claude Code, and other agents; defer install instructions and compatibility claims until their supported skill paths, tooling, and behavior are checked separately.
