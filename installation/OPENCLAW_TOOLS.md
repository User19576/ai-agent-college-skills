# OpenClaw tool map for the college skills

Verified against OpenClaw's [tools overview](https://docs.openclaw.ai/tools), [source tool catalog](https://github.com/openclaw/openclaw/blob/main/src/agents/tool-catalog.ts), and the linked implementations below. These are **OpenClaw** tool names, not Hermes skill names. A skill does not grant tool access: profile, allow/deny policy, provider, sandbox, and model can remove tools from a turn.

| Workflow need | OpenClaw tool | Source / limitation |
| --- | --- | --- |
| List a folder | `ls` | [Directory tool](https://github.com/openclaw/openclaw/blob/main/src/agents/sessions/tools/ls.ts#L46-L63); not recursive search. Use an approved local search command via `exec` if needed. |
| Read text or a local image | `read` | [File tool](https://github.com/openclaw/openclaw/blob/main/src/agents/sessions/tools/read.ts#L357-L379); supports text paging and images. [Binary documents are not returned](https://github.com/openclaw/openclaw/blob/main/src/agents/sessions/tools/read.ts#L438-L455). |
| Inspect an image/screenshot | `view_image` | [Image tool schema](https://github.com/openclaw/openclaw/blob/main/src/agents/tools/image-tool.ts#L290-L311): `path` or `paths` and optional `prompt`. No crop argument; create a separate crop/render with a permitted tool if needed. |
| Analyze PDF contents | `pdf` | [PDF tool](https://docs.openclaw.ai/tools/pdf) and [source schema](https://github.com/openclaw/openclaw/blob/main/src/agents/tools/pdf-tool.ts#L80-L91). Provider/model and page limits apply. An analysis result is not a complete visual export check. |
| Parse DOCX or render pages | Available local parser/converter via `exec` | OpenClaw `read` [rejects binary documents](https://github.com/openclaw/openclaw/blob/main/src/agents/sessions/tools/read.ts#L449-L454). Check for an installed permitted converter; do not assume a `docx` tool or fabricate a render. |
| Read/write/edit files | `read`, `write`, `edit`, `apply_patch` | [File tool catalog](https://github.com/openclaw/openclaw/blob/main/src/agents/tool-catalog.ts#L91-L100); `write` overwrites, `edit` does exact replacements, [`apply_patch`](https://docs.openclaw.ai/tools/apply-patch) does structured patches. Read first and respect scope. |
| Hash, move, convert, recursive search | `exec` | [Exec docs](https://docs.openclaw.ai/tools/exec), [exec schema](https://github.com/openclaw/openclaw/blob/main/src/agents/bash-tools.schemas.ts#L26-L86). Approval and host policy apply. On Windows OpenClaw's host exec [prefers PowerShell](https://docs.openclaw.ai/tools/exec), not Git Bash syntax by default. |
| Look up sources | `web_search`, `web_fetch` | [Web docs](https://docs.openclaw.ai/tools/web); `web_search` may not appear without a configured provider. Cite retrieved primary sources. |
| Read another installed skill | `skills_read` if visible | [Tool catalog](https://github.com/openclaw/openclaw/blob/main/src/agents/tool-catalog.ts#L202-L215). Never assume a Hermes `pdf`, `docx`, or `grounded-citations` skill is installed on OpenClaw. |

These tools were checked in documentation and upstream source, not executed in this repository: no OpenClaw runtime is available here. Validate actual exposure and PDF/DOCX rendering in the selected OpenClaw agent before relying on a complete coursework review.
