# Operational memory

vault:/home/galgo/Obsidian/Codex-System
entry:/home/galgo/Obsidian/Codex-System/INDEX.md
canonical_state:/home/galgo/Obsidian/Codex-System/SYSTEM.md
validator:/home/galgo/.codex/bin/codex-notes-validate
mcp:obsidian;profile:context;activate:on-demand

## Retrieval

default:INDEX.md
next:follow 1-3 task-relevant [[links]] only
system:SYSTEM.md only for machine/system facts
session:Session.md for recovery, post-compaction resume, or active work handoff
forbid:full-vault injection,eager traversal,unrelated sections
routes:mcp->MCP.md;boot|kernel|memory|network|services|wm|gpu|storage->SYSTEM.md;file->HOT_FILES.md;recovery->RECOVERY.md;install->INSTALL.md;ssh->SSH.md;resume->Session.md

Before mutation:

1. identify component
2. load the canonical component note
3. load only linked history needed for compatibility or rollback
4. mutate

After meaningful mutation:

1. update canonical fact
2. append CHANGES entry
3. retain newest 100
4. update HOT_FILES count,last,history,links
5. add rollback when possible
6. run `codex-notes-validate --trim`

read-only:no change entry
change_filter:meaningful mutations only
hot_candidate:changes>=2 in retained window OR critical
hot_limit:20
fact_ownership:one canonical note;other notes link
style:key:value;paths;commands;ids;links;minimal prose
checkpoint:follow `/home/galgo/.codex/rules/tokensSave.txt.md`;rewrite Session.md;never store secrets

## Graph invariants

links:no broken targets or anchors
reachability:all notes from INDEX.md
changes:max100;unique ids;oldest dropped on overflow
hot_files:max20;existing paths;derived counters
index:last_change=newest id
facts:no exact duplicate across canonical notes
stale:update or remove during related mutation

## Vault scope

global:one system vault
project:one isolated project vault when project memory is required
project_retrieval:load project entry only when relevant
fallback:direct Markdown access when Obsidian MCP unavailable and operation is filesystem-complete
