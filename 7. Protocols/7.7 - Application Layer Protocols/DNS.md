# DNS — Domain Name System

🗓️ M/Y: Jul-25  
📂 Category: Protocols

---

## What is DNS?

DNS is like the **phonebook of the internet**.  
It takes that confusing IP address like `142.250.183.110` and gives it a nice, friendly name like `google.com`.

So we type `youtube.com`, but DNS is doing the dirty work behind the scenes, asking,  
> "Hey, what IP does this name point to?"

And once it finds the IP, our browser connects to that server. Boom. Site loads.

---

## Why do we need DNS?

- We can’t remember 1000s of IPs. (unless our brain runs BGP tables)
- Websites often change their IPs.
- DNS helps maintain **flexibility, speed, and organization**.

---

## How does DNS work? (Simple Walkthrough)

1. **We type `reddit.com` in our browser.**
2. Our browser checks **local DNS cache** first.
3. If not found → asks our **OS**, which checks its own cache.
4. If still not found → a DNS query is sent to the **DNS resolver** (usually from our ISP or a custom one like Google DNS, NextDNS or Cloudflare).
5. The resolver checks with:
   - **Root DNS servers**
   - Then **TLD servers** (e.g. `.com`, `.org`)
   - Then the **authoritative nameserver** for `reddit.com`
6. The final IP address is returned.
7. Now our browser says: “Thanks!” and connects directly to that IP.

---

## Types of DNS Servers

| Type | Purpose |
|------|---------|
| **Root Server** | Top level — directs us to TLDs (.com, .org, etc) |
| **TLD Server** | Directs to the right nameserver for domain |
| **Authoritative Server** | The final boss — gives the real IP |
| **Recursive Resolver** | Does all the lookup dirty work on our behalf (usually ISP DNS) |

---

## Example in Real Life

Us: `openai.com`  
DNS: “lemme check…”  
Root → .com → `openai.com` → IP: `104.18.12.123`  
Then our device: “sweet” → connects → loads site.

---

## DNS in CLI

- `nslookup google.com`
- `dig reddit.com`
- `host github.com`

These give us the IP and DNS response info.

---

## DNS Leaks?

- Happens when our browser or OS sends DNS requests **outside our VPN**.
- Our ISP still sees what websites we're visiting, even if traffic is encrypted.
- That’s why **DNS leak protection** matters in privacy.

---


## DNS over HTTPS (DoH) / DNS over TLS (DoT)

- Encrypts our DNS queries.
- Prevents snooping or MITM modification.
- Browsers like Firefox and Chrome support DoH (e.g. via Cloudflare).

---

## DNS Hijacking / Poisoning (Just a Glimpse)

- **What Happens**:  
  An attacker modifies DNS responses, tricking our system into connecting to a fake website.

- **Example**:  
  We type `paypal.com`, expecting IP `77.77.77.77`.  
  The attacker’s poisoned DNS responds with a fake IP, redirecting us to a lookalike malicious site.

- **Goal of Attack**:  
  - Steal credentials  
  - Deliver malware  
  - Perform man-in-the-middle (MitM) attacks

- **Defense Tips**:
  - Use **trusted DNS providers** (e.g., Cloudflare `1.1.1.1`, Google `8.8.8.8`)
  - Enable **DNSSEC** (Domain Name System Security Extensions)
  - Use a **VPN** to encrypt DNS queries and avoid ISP/man-in-the-middle tampering


## Summary
DNS is the middleman that tells our device “where to go” on the internet — it translates human words into numbers, like our own Google Maps of the net.

---

*“Without DNS, we'd be memorizing IPs like we are living in 1995. No thanks.”*
