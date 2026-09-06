# Agent and model rules

Default to the current agent and current model. Do not spawn or escalate when the current agent can complete the next concrete step.

Use additional agents only for independent work whose quality or time benefit exceeds model context RAM and coordination cost. Normal maximum is two active AI workers including the primary agent.

Use architecture agents only for genuinely non-trivial design. When an agent is provided through an MCP load `mcp.txt.md` for its lifecycle and limits.

Escalate the model only after a focused attempt with better local context fails or the task requires difficult architecture subtle concurrency mathematics or another high-risk decision.

Give an agent only its task constraints relevant files current findings proposed solution and open question. Terminate it when finished.
