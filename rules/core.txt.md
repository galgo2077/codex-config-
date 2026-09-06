# Core rules

Correctness first. Then security, data integrity, simplicity, maintainability, token/resource use, and speed.

Use KISS and YAGNI. Prefer deleting reusing or modifying existing work. Write only what the request needs. Default to one agent one task and sequential execution.

Token and context economy: follow `tokensSave.txt.md`. Credential handling: follow `credentials.txt.md`.

## Minimum work

Act autonomously when the next safe step is discoverable. Ask only for unavailable credentials, irreversible choices, product decisions, or physical intervention.

For simple config prompt or documentation work:

read target → edit → smallest relevant validation → inspect relevant diff → done

Stop when the requested behavior works and no material risk remains. Do not continue with unrelated cleanup or hypothetical improvements.
