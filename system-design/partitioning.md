# 🧩 Partitioning (Sharding)

## What it is
Splitting a database into smaller pieces (shards) to scale horizontally.

---

## Types

### Horizontal Partitioning
- Rows split across shards

Example:
- Users A–M → Shard 1
- Users N–Z → Shard 2

---

### Vertical Partitioning
- Columns split into different tables

Example:
- User profile data
- User activity data

---

## Sharding Strategies

### Hash-based
hash(user_id) % N

### Range-based
Based on value ranges

### Directory-based
Lookup service maps keys to shards

---

## Pros
- Scales databases
- Reduces load per node

## Cons
- Hard joins
- Rebalancing is difficult
- Hotspots possible
