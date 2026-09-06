# Context filtering

Start with the project index or system note, follow only 1–3 task-relevant links, then search exact symbols or paths before reading files. Expand only when evidence requires it.

`.codexignore` is a human/agent exploration policy, not a native Codex filter or security boundary. If an existing Git project has one, run `/home/galgo/.codex/bin/codex-ignore-sync` once per session and again only if it changes. Do not create one merely to begin work. If sync fails, use `/home/galgo/.codex/bin/codex-context-rg`, which applies it directly.

Use `rg --files`/`rg` with known paths, or the context helpers when `.codexignore` applies. Respect `.gitignore`. Avoid `.git`, dependencies, generated output, caches, environments, large data, and logs unless the task requires them.

Do not use `find PROJECT_ROOT`, `grep -R PROJECT_ROOT`, `rg --no-ignore`, `rg -uuu`, custom recursive walkers, or broad unfiltered crawls unless ignored data is explicitly required.

Root/global `AGENTS.md` is already injected. Do not reread it unless changed. Do not send whole repositories or vaults to agents/MCPs, and do not duplicate context between them.
