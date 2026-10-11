# Rule router

Read this router once per session. Load each `Always` rule once, in order. Load no specialized module until its trigger applies. A task may trigger multiple modules.

| Trigger | Load |
|---|---|
| Always | `core.txt.md`, `tokensSave.txt.md`, `credentials.txt.md` |
| Project exploration, file discovery, recursive search, agents, MCP, Ponytail, or Roundtable context | `context.txt.md` |
| MCP configuration RAM process or lifecycle | `mcp.txt.md` |
| Architecture additional agents or model escalation | `agents.txt.md` |
| Code modification requiring validation | `coding.txt.md` |
| Performance RAM CPU latency throughput concurrency or algorithm optimization | `performance.txt.md` |
| Authentication authorization secrets permissions user input destructive work or financial execution | `security.txt.md` |
| Git operation checkpoint commit or history manipulation | `git.txt.md` |
| Bug failure or unexpected behavior | `troubleshooting.txt.md` |
| External documentation upstream behavior or current information | `web.txt.md` |
| System administration or hardware | `system.txt.md` and `comands.txt.md` |
| Recovery rollback or data restoration | `recovery.txt.md` |
| SSH work | `ssh.txt.md` |
| Explicit vault or project-context need | `obsidian.txt.md` |
| Dependency change | `dependencies.txt.md` |
| File layout move rename or deletion | `files.txt.md` |
| New project creation | `project.txt.md` |
| Explicit code review or cleanup | `review.txt.md` |
| Explicit writing or output-format work | `writing.txt.md` and `output.txt.md` |

Examples: typo or small config edit loads core only. Normal code fix loads core and coding. Bug loads core troubleshooting and coding. Performance work adds performance. Sensitive work adds security. MCP resource work loads core and mcp.

Never load a module just in case. Never treat module availability as a requirement to use its tools.

Project bootstrap flow: read the project index, then follow `context.txt.md`. Do not load a project vault, repository, Git history, MCP, or specialized rule merely because it exists.

For project work, the nearest applicable project `AGENTS.md` adds project-specific constraints. On a direct conflict with these shared rules, follow that project instruction unless a higher-level instruction applies, and report the conflict and resolution to the user.

`tasks.txt.md` is a compatibility pointer only. Do not load it.
