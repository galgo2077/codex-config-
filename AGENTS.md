# Codex bootstrap

Before every task:

1. Read `/home/galgo/.codex/rules/bootstrap.txt.md` and every rule it lists.
2. Verify the required rule files and MCP health.
3. Load `/home/galgo/Obsidian/Codex-System` context plus project vault context when inside a project.
4. Inspect the local system and current Git state, then decompose the task.
5. Use the minimum useful multi-agent team by default.

Do not write project code until bootstrap passes. If a required MCP fails, repair and verify it before resuming from the last safe state.
