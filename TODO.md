# To-do

## OpenClaw adaptations — after Hermes readiness

- Project standard: finish the corresponding Hermes skill work first, then adapt it for OpenClaw as a separate follow-up phase. Do not treat OpenClaw parity as a prerequisite for completing Hermes work.
- Once the current Hermes academic-support and export-verification work is ready, adapt its reusable improvements into the corresponding `openclaw-skills/` copies. Keep OpenClaw-native tools and verify capabilities separately; the current Hermes changes have not yet been ported.

## OpenClaw document skills

- Revisit whether to port the Hermes `docx` and `pdf` skills to OpenClaw. Inspect their scripts, references, dependencies, and licensing; adapt Hermes tool names to OpenClaw tools. Compare the `pdf` skill with OpenClaw's native `pdf` tool, and verify DOCX parsing and rendering on an actual OpenClaw runtime before adding installation instructions or claiming support.

## Rework `caveman` skill section

- Reword and redesign the `caveman` section — `cave` skills repo has been overhauled since initial install, needs new instructions, clarification between full cave setup (proxy, mcp, skills etc.) and just cave skills.

See [COMPLETED_TODO.md](COMPLETED_TODO.md) for completed work and other deferred agent ports.
