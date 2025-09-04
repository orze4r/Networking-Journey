# VPN (Virtual Private Network)

🗓️ M/Y: Jul-25  
📂 Category: Core Concepts  

---

## What the hell is a VPN?

**VPN = Virtual Private Network**

It’s basically like a secure tunnel between me and the internet.  
When I connect to a VPN, it wraps my internet traffic in a secret envelope and sends it through a private tunnel — hiding it from my ISP, school, coffee shop Wi-Fi, or that sketchy neighbor sniffing traffic.

---

## 🕳️ So what does it actually do?

✅ Hides my **real IP address**  
✅ Encrypts my **traffic**  
✅ Routes all data through a **VPN server**  
✅ Bypasses **geo-restrictions**, censorship, and firewalls  
✅ Can *sometimes* make my internet safer — but not always

---

## How it works (basic brain mode)

Let’s say I connect to `instagram.com`

- Without VPN:
  - Your traffic goes:  
    **Me → ISP → Instagram servers**  
    Everyone in-between can see my IP and traffic (unless HTTPS)

- With VPN:
  - My traffic goes:  
    **Me → Encrypted tunnel → VPN Server → Instagram**  
    My ISP only sees I'm connected to a VPN. That’s it.

---

## 🎭 What people usually use VPNs for:

- 🔒 **Privacy** from ISP, network admin, government
- 🌍 **Change location** (like appearing from Japan while sitting in Delhi)
- 📺 **Unblock content** (like Netflix, BBC, etc)
- 🧅 **Add a layer of anonymity** when browsing or using Tor
- 🚫 **Avoid censorship** in restricted countries
- 😏 **You know what…**
---

## What a VPN **is not**:

- ❌ A hacker shield  
- ❌ A malware remover  
- ❌ Full anonymity guarantee  
- ❌ A one-size-fits-all security tool  

If my device is leaking info, no VPN will save me.

---

## VPN Protocols (just the names for now)

- **OpenVPN** – reliable and open-source
- **WireGuard** – new, fast, lightweight
- **IKEv2/IPSec** – stable for mobile, used in VPNs like Windscribe, etc.
- **L2TP/IPSec** – older, still used sometimes
- **SSTP / PPTP** – forget these unless I'm stuck in 2008

---

## DNS Leaks and Other Warnings

Even with VPN on, stuff can leak:

- ❗ DNS Leaks (my system still uses my real ISP DNS)
- ❗ WebRTC Leaks (browser feature leaking my IP)
- ❗ Fingerprinting (browser config reveals my identity)

**→ Use browser hardening + DNS leak protection + disable WebRTC.**

---

## Bonus: Split Tunneling

I can make **some apps** use VPN and **some use regular internet.**  
Useful for:

- Downloading large files with real IP
- Watching local content while still securing other traffic

---

