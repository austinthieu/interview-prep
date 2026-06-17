# 🔄 Data Replication Models

## Active : Passive (Primary-Standby)

### How it works
- One active node handles all traffic
- One passive node is backup

### Pros
- Simple
- Strong consistency

### Cons
- Underutilized resources
- Failover delay

---

## Active : Active

### How it works
- Multiple nodes handle traffic simultaneously

### Pros
- High availability
- Better scaling
- Multi-region support

### Cons
- Conflict resolution needed
- Complex consistency handling
