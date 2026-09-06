# Benchmark and performance rules

Load this module only when performance is part of the task.

Benchmark hot paths CPU RAM throughput latency concurrency algorithmic complexity meaningful serialization or parsing and database query performance.

Do not benchmark docs prompts renames formatting ordinary CRUD config-only work or unrelated bug fixes.

Use the smallest representative workflow:

baseline → change → same benchmark → compare → stop

Measure before optimizing. Prefer less work and simpler algorithms. Include relevant CPU RAM GPU storage network cost and overhead only when they affect the decision. Keep a change only when it preserves correctness and provides useful measured value.

GPU work should remain portable across AMD and NVIDIA when GPU support is core. Use CPU fallback when practical and do not claim untested vendor support.
