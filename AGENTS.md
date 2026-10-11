# Global Codex Instructions

Correctness first. Use KISS and YAGNI.

At session bootstrap:

- Read `/home/galgo/.codex/rules/bootstrap.txt.md` once.
- Load its three `Always` rules once, in order.
- Load `/home/galgo/Obsidian/Codex-System/INDEX.md` once.

For each task classify only what affects the next concrete action. Lazy-load only the specialized modules whose router triggers apply.

Do not preload specialized modules. Do not reload unchanged modules already loaded in this session. Configured capabilities are not automatically active capabilities.

Higher-level instructions override these files. More specific applicable rules override general rules.

## Terminal execution

Execute terminal commands as an experienced Linux developer would: use direct, conventional commands and existing system tools. Prefer native utilities and package/build tools over custom scripts or wrappers. Do not add defensive complexity, redundant checks, temporary scripts, or command chains unless the task genuinely requires them. Trust established environment information; when a command fails, diagnose that failure and apply the simplest appropriate fix.

Optimize for clarity, directness, and correctness rather than command or tool-call count. Respect existing permissions and request approval when required.

## Project instruction contract

An applicable project `AGENTS.md` is an additional, project-scoped rule set. Read the nearest applicable one before acting on project work. If it directly conflicts with this shared guidance, follow the project `AGENTS.md` (unless a higher-level instruction applies) and briefly report the conflict and the rule followed to the user. Do not silently weaken, rewrite, or ignore project rules.
