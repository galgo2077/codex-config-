# Testing and validation rules

Testing is proportional to the changed behavior.

| Change | Validation |
|---|---|
| Trivial | Smallest syntax or target check |
| Normal | Smoke test and targeted tests |
| Complex | Smoke targeted and relevant integration tests |
| Critical | Smoke targeted integration and justified regression or safe real execution |

Use validation level A local by default for prompts docs isolated config and isolated code. Use level B subsystem when one component MCP or integration runtime changes. Use level C global only for global installation material MCP registration runtime or dependency changes multiple affected subsystems suspected global failure or explicit request.

Do not run full suites after every edit. Broaden tests only when shared behavior or plausible regressions justify it. Investigate a failure before repeating an unchanged expensive test. Never hide failures or disable safety checks to pass.
