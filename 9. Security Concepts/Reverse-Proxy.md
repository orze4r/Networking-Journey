# Reverse Proxy

🗓️ M/Y: Jul-25  
📂 Category: Security Concepts  

---

## What is a Reverse Proxy?

**Reverse Proxy = A server that stands in front of your actual servers.**  
It handles all incoming requests *before* they reach the backend servers.

Instead of:

> User → Server

It becomes:

> User → Reverse Proxy → Actual Server

It’s like a super picky receptionist that only lets the right people into the building.

---

## Why is it called "Reverse"?

Because a **normal proxy** hides the *client*.  
But a **reverse proxy** hides the *server(s)*.

| Type | Hides |
|------|-------|
| Proxy | The **user's** identity |
| Reverse Proxy | The **server's** structure/backend |

---

## What does it do?

✅ Accepts and forwards traffic to backend servers  
✅ Balances traffic between multiple servers  
✅ Caches content  
✅ Adds extra security (firewall, DDoS protection, etc.)  
✅ Can terminate SSL/TLS (handle HTTPS)  
✅ Hides internal infrastructure

---

## Real-World use cases

- **Load Balancer**  
  → Distributes traffic across multiple backend servers to prevent overload.

- **SSL Termination**  
  → Handles HTTPS encryption, offloads heavy crypto work from backend.

- **Web Acceleration**  
  → Caches responses to reduce load and speed things up.

- **Security Shield**  
  → Filters out malicious traffic or rate-limits requests.

---

## Tools used as reverse proxies

- **Nginx** 🥇 (super lightweight and powerful)
- **HAProxy** (made for high availability/load balancing)
- **Apache HTTPD** (can act as one)
- **Cloudflare** (a global reverse proxy for millions of websites)

---

## Think of it like...

🧍‍♂️ User: “Hey server, give me the website!”  
🛡️ Reverse Proxy: “Sure… let me clean this request, route it, cache it, and encrypt it first.”  
🏢 Backend Server: “Thank you for not letting the bots in.”

---

## Summary

**Reverse Proxy = Gatekeeper for my servers.**  
Used to load balance, cache, secure, and protect backend services.

If a **proxy** is for *me* (the user),  
then a **reverse proxy** is for *the website owner*.

---
---

## 🖼️ Visual Example

```mermaid
graph LR
    A[User] --> B[Reverse Proxy]
    B --> C[Server 1]
    B --> D[Server 2]
    B --> E[Server 3]
