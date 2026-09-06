# MCP resource rules

Configured does not mean running.

Keep useful MCPs installed and configured. Optional MCPs running while idle should be zero. Use built-in tools when they cover the next action.

Lifecycle:

need capability → start or reuse MCP → focused action → extract compact result → terminate or release MCP

Use one expensive MCP by default. Use two only when genuine cooperation is required. Cheaply reuse a usable live instance before creating another. Do not build a custom supervisor.

Ponytail is for genuinely non-trivial architecture only. Start it for one proposal then stop it after the decision.

Roundtable uses one reviewer by default. A second reviewer is allowed only for critical or high-risk work. Use at most two debate rounds. Stop when material disagreement is resolved. Keep no critics alive during coding or testing.

Context7 is only for uncertain library API or version behavior. Query narrowly retain only useful facts then release it.

Browser Playwright Puppeteer and DevTools are only for real browser behavior. Do not start them for backend static or configuration tasks. Close browser contexts and processes after validation.

Avoid duplicates caused by retries reconnects stale sessions repeated reviewers equivalent browser tools or duplicate runtimes.

When RAM is high:

1. Stop completed workers.
2. Remove duplicate instances.
3. Stop browser and DevTools workers.
4. Stop documentation workers.
5. Stop completed planning and review workers.
6. Reduce Roundtable reviewers.
7. Compact retained output.
8. Restart a leaking MCP when needed.

When MCP configuration or runtime changes also load `coding.txt.md` for the canonical validation levels.
