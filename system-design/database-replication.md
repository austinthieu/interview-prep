# 📡 Database Replication

## What it is

Database replication is copying data from one database (primary) to one or more replica databases to improve availability, scalability, and fault tolerance.

---

## Types of Replication

### 1. Single Leader (Primary-Replica)

- One primary handles writes
- Replicas handle reads

**Flow:**
Write → Primary → Replicas sync

**Pros:**

- Simple
- Read scalability
- Backup support

**Cons:**

- Write bottleneck
- Replication lag (stale reads)

---

### 2. Multi-Leader

- Multiple databases accept writes

**Pros:**

- High availability
- Multi-region writes

**Cons:**

- Conflict resolution needed
- Complex consistency

---

### 3. Leaderless

- No central leader
- Writes go to multiple nodes

**Pros:**

- Very high availability

**Cons:**

- Complex consistency model

---

## Key Concept

Replication lag = delay between primary update and replica update
