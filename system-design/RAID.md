# 💾 RAID (Redundant Array of Independent Disks)

## What it is
RAID is a method of **combining multiple physical disks into a single logical unit** to improve:
- Performance
- Fault tolerance
- Storage reliability

---

# 🧠 Why RAID is used
- Disks fail (hardware is unreliable)
- Need faster read/write performance
- Need data redundancy (backup protection)
- Improve uptime in servers

---

# ⚙️ Core Ideas

## 1. Striping
- Data is split across multiple disks
- Improves performance

## 2. Mirroring
- Data is duplicated on multiple disks
- Improves reliability

## 3. Parity
- Extra calculated data used for recovery
- Balances storage efficiency + redundancy

---

# 📊 Common RAID Levels

---

## 🟢 RAID 0 (Striping only)

### How it works
- Data split across multiple disks
- No redundancy

### Pros
- Very fast read/write
- Full disk capacity usable

### Cons
- No fault tolerance
- If 1 disk fails → all data lost

### Use case
- High-performance, non-critical workloads (e.g., temp processing)

---

## 🔵 RAID 1 (Mirroring)

### How it works
- Exact copy of data on 2+ disks

### Pros
- High reliability
- Simple recovery (just use mirror)
- Fast reads (can read from multiple disks)

### Cons
- 50% storage efficiency
- Expensive (duplicate storage)

### Use case
- Critical systems, small databases

---

## 🟡 RAID 5 (Striping + Parity)

### How it works
- Data + parity distributed across disks
- Requires at least 3 disks

### Pros
- Good balance of performance + redundancy
- Can survive 1 disk failure

### Cons
- Write performance slower (parity calculation)
- Rebuild time can be long

### Use case
- General-purpose servers

---

## 🟠 RAID 6 (Double Parity)

### How it works
- Like RAID 5 but with 2 parity blocks
- Requires at least 4 disks

### Pros
- Can survive 2 disk failures
- Very safe

### Cons
- Slower writes than RAID 5
- More storage overhead

### Use case
- Enterprise storage systems

---

## 🔴 RAID 10 (1+0 Mirror + Stripe)

### How it works
- Mirror pairs, then stripe across them

### Pros
- Very fast
- Very reliable
- Fast rebuilds

### Cons
- 50% storage efficiency
- Requires many disks

### Use case
- High-performance databases
- Financial systems

---

# ⚖️ RAID Comparison

| RAID | Type | Fault Tolerance | Performance | Storage Efficiency |
|------|------|----------------|-------------|--------------------|
| RAID 0 | Striping | ❌ None | ⭐⭐⭐⭐⭐ | 100% |
| RAID 1 | Mirroring | ✔ 1 disk per mirror | ⭐⭐⭐ | 50% |
| RAID 5 | Striping + parity | ✔ 1 disk | ⭐⭐⭐⭐ | High |
| RAID 6 | Double parity | ✔ 2 disks | ⭐⭐⭐ | Medium |
| RAID 10 | Mirror + stripe | ✔ multiple (depends) | ⭐⭐⭐⭐⭐ | 50% |

---

# 🧠 Quick Memory Tricks

- RAID 0 = Fast but risky
- RAID 1 = Copy (safe but expensive)
- RAID 5 = Balanced
- RAID 6 = Extra safe
- RAID 10 = Fast + safe (best of both worlds)

---

# 🚀 Real-world usage

- Databases → RAID 10
- File storage → RAID 5 or 6
- Caching systems → RAID 0 sometimes
- Enterprise systems → RAID 6

---

# ⚠️ Important Note

RAID is NOT a backup system.

It protects against disk failure, but not:
- Accidental deletion
- Corruption
- Malware
- Logical errors

---

# 🔥 Interview insight

Modern systems often combine RAID with:
- Cloud storage replication (S3-style systems)
- Distributed storage (HDFS, Ceph)
- Multi-region redundancy
