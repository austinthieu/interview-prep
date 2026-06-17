# ⚖️ Load Balancing Technologies

## What it is
Load balancing distributes incoming traffic across multiple servers.

---

## Layers of Load Balancing

### Layer 4 (Transport)
- Works on IP + TCP
- Fast and simple

**Examples:**
- HAProxy (TCP mode)
- AWS NLB

---

### Layer 7 (Application)
- Works on HTTP data
- Smart routing based on URL, headers, cookies

**Examples:**
- NGINX
- AWS ALB
- Cloudflare

---

## Features
- Health checks
- SSL termination
- Routing rules
- Geo routing

---

## Key Idea
L4 = fast routing  
L7 = smart routing
