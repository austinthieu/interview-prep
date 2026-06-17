# ⚡ In-Memory Caching

## What it is
Storing frequently used data in RAM for fast access.

---

## Why it matters
- RAM is extremely fast (microseconds)
- Reduces database load
- Improves response time

---

## Common Tools
- Redis
- Memcached

---

## Cache Patterns

### Cache Aside (Most common)
App checks cache → miss → DB → store in cache

### Write Through
Write to cache + DB simultaneously

### Write Back
Write to cache first, DB later

---

## Pros
- Very fast reads
- Reduces DB load

## Cons
- Cache invalidation is hard
- Stale data risk
