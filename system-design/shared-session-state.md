# 🍪 Shared Session State

## What it is
Shared session state is a way to **store and access user session data across multiple servers** in a distributed system.

Instead of keeping session data on one server, it is stored in a **central/shared storage layer** so any server can retrieve it.

---

# 🧠 Why it exists

In a single-server app:
- Session data is stored in memory (easy)

In a scaled system (multiple servers):
- User A logs in on Server 1
- Next request goes to Server 3
- Server 3 doesn’t know who User A is ❌

➡️ Solution: Shared session state

---

# 🏗️ How it works

1. User logs in
2. Server creates session data (userId, auth info, etc.)
3. Session is stored in a shared store
4. A session ID is sent to the client (usually via cookie)
5. On future requests:
   - Client sends session ID
   - Any server retrieves session from shared store

---

# 🗄️ Common Session Stores

- Redis (most common)
- Memcached
- Database (less common, slower)
- DynamoDB / cloud KV stores

---

# 🔁 Typical Flow

Client → Load Balancer → Server A/B/C  
                               ↓  
                       Shared Session Store (Redis)

---

# ⚖️ Why shared session state is needed

## Without it (bad in distributed systems)
- Sessions stored locally per server
- User gets randomly routed
- Session breaks frequently
- Requires sticky sessions (not ideal)

## With it (good)
- Any server can handle any request
- Fully supports horizontal scaling
- Better fault tolerance

---

# 🍪 Sticky Sessions vs Shared Session State

| Feature | Sticky Sessions | Shared Session State |
|--------|----------------|----------------------|
| How it works | User stays on same server | Session stored centrally |
| Scalability | Limited | High |
| Reliability | Poor (server crash = session lost) | Good |
| Complexity | Low | Medium |
| Preferred | Small systems | Large systems |

---

# 🚫 Problems with shared session state

## 1. Latency
- Extra network call to session store

## 2. Single dependency
- If Redis goes down → login system breaks

## 3. Consistency issues
- Multiple servers updating session data

---

# ⚡ Optimization techniques

- Use Redis clustering
- Replication + failover
- Set TTL (auto-expire sessions)
- Keep session data minimal

---

# 🧠 Quick Memory Trick

- Sticky session = “user sticks to one server”
- Shared session = “all servers share one brain”

---

# 🚀 Real-world usage

Most modern systems use:
- Load balancer + stateless servers
- Redis-based shared session store
- JWT sometimes instead of server sessions

---

# 🔥 Interview insight

Modern systems often try to **avoid server-side sessions entirely** using:
- JWT (stateless auth)
- OAuth tokens

But shared session state is still common in:
- Enterprise apps
- Legacy systems
- High-security systems needing session revocation
