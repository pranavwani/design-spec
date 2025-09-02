# Low-Level Design (LLD)

- **SDK**:
  - `CacheClient.get(key)` → returns cached value or `null`
  - `CacheClient.set(key, value, ttl)` → sets value with TTL
- **Foundry**:
  - Hooks into ORM write ops → invalidates cache.
