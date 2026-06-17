# 🍪 Session Affinity (Sticky Sessions)

## What it is
Session affinity ensures a user is always routed to the same server.

---

## How it works
- Load balancer assigns a server
- Stores mapping via cookie or IP hash
- Future requests go to same server

---

## Pros
- Simple session handling
- No shared session store needed

---

## Cons
- Uneven load distribution
- Poor fault tolerance
- Limits horizontal scaling

---

## Why it's used
- Legacy systems
- No centralized session storage
