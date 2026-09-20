# Offline Sync Conflict
Optimistic versioning backend. Each operation carries deviceId, operationId, itemId and baseVersion. Exact-current updates are accepted, stale non-overlapping field updates are merged, and stale overlapping updates return CONFLICT. operationId makes retries idempotent. Includes history endpoint.

POST /sync, GET /items/:id, GET /items/:id/history, GET /health.