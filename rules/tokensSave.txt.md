# TOKENS SAVE — mandatory

Goal: minimize cumulative token/quota use without reducing correctness, security, scope, or required validation.

## Core
- Optimize MODEL↔TOOL CYCLES first. Batch independent, read-only, conflict-free checks into one exec/tool round and run concurrently. Keep writes, dependencies, approvals, adaptive/stateful work serial.
- Never repeat a completed check unless its inputs changed. Do not poll every second; wait an appropriate interval.
- Start narrow: exact symbol/file/test/path. Broaden only when evidence requires it.
- Root/global `AGENTS.md` already injected by Codex: do not reread unless changed. Read bootstrap/index/system/rules once/session; reuse conclusions.
- Never dump repo/large files/logs/generated/vendor/dependency trees by default. Use `rg`, exact ranges, `head/tail`, `jq` fields, `--quiet`, `--short`, `--name-only`, `--stat`.
- Redirect verbose output to `/tmp`/log; read only relevant/failing slices.
- Git: `status --short` → `diff --stat/--name-only` → targeted diff/history. After successful patch, verify edited region or tests; do not reread whole file.

## Tests
- Edit loop: smallest relevant test/lint.
- Logical milestone: affected suite once.
- Full lint/test/security/benchmark only at explicit gates/final validation.
- Do not rerun unchanged passing suites. Benchmark only measured/suspected hot paths.

## Rolling context checkpoint
Maintain ONE concise checkpoint (`Vault/Session.md` or project equivalent), REWRITE instead of append, target <=1200 tokens:
`objective | acceptance gates | invariants/decisions | relevant/changed files | exact test status | blockers/risks | next 1–5 actions`.
Never store narration, raw logs, dead hypotheses, repeated summaries, or completed exploration.

### When to clean context
If `/status` exposes usage:
- <60% used: normal targeted work.
- 60–75%: stop broad exploration; refresh checkpoint before next phase.
- 75–85%: finish atomic step → checkpoint → `/compact` at phase boundary.
- >85%: do not start large work → checkpoint → compact or new thread.

Start a FRESH THREAD even earlier when task changes substantially, stale/contradictory assumptions dominate, completed work dominates history, repeated compactions inflate context, or another compaction would soon be needed.
Before compact/new: update checkpoint. After: load checkpoint + applicable instructions only; never rediscover whole repo.
Never compact mid migration/order/deployment/destructive operation unless forced.

## Agents
- Spawn only for genuinely independent work that reduces parent cycles.
- No duplicate repo/domain scans across agents.
- Parallelize independent read-only investigations.
- Require terse report: `root cause | evidence/files | fix | tests | blocker`.
- Parent reuses findings; do not redo searches.

## MCP / plugins / web
- Keep only task-relevant MCP servers/tools active; prefer `enabled_tools` allow-lists and disable rare servers in lean profiles.
- Do not repeatedly enumerate/reload MCP catalogs. Start/use MCP only when needed.
- Web only for current/external facts, official docs/API compatibility, or explicit research; never research what local code/tests already prove.
- Batch independent searches; stop after sufficient authoritative evidence.

## Knowledge / files
- Durable compact rules → `AGENTS.md`; active session state → checkpoint; detailed history/evidence → Vault loaded on demand.
- Keep always-loaded instructions small and deduplicated; link to detail instead of embedding it.
- `.codexignore` is NOT a reliable/native Codex exclusion boundary. Do not rely on it. Respect `.gitignore`; avoid ignored/generated files unless needed. Use filesystem permission deny-rules for secrets when available.

## Coding / output
- Root-cause fix, smallest coherent patch. No unrelated refactor, speculative wrappers, duplicate implementations, unnecessary dependencies/docs/comments/tests.
- Prefer deleting obsolete paths over maintaining parallel logic when safe.
- No repeated progress narration. Group actions. Final default: `changed | validated | blockers/next`.
- Never paste large logs/code/test output unless requested.

## Reasoning policy
- Minimal/low: lookup, formatting, known commands, tiny edits.
- Medium: normal implementation/debugging.
- High/xhigh only: hard architecture, concurrency, security, numerical correctness, destructive migrations, unresolved failures.
- Default verbosity low. Save tokens by removing redundant context/cycles before lowering reasoning.

## Safety priority
Never save tokens by skipping required tests, security/RLS/ownership checks, migrations, exchange safeguards, backups, or destructive-operation verification.
Priority: correctness > security > data integrity > reproducibility > token efficiency > speed.
