# WAN (Wide Area Network)

🗓️ M/Y: Jul-25  
📂 Category: Network Types - Wide or Specialized Networks

---

## What is a WAN?

**WAN = Wide Area Network**  
This is *not* our cozy little LAN. This is the real-world mess where our internet lives.

WANs cover **cities**, **countries**, and even **continents**.  
Think: ISPs, undersea cables, [satellites](https://github.com/bwbearr/Field-Notes/blob/11a39d8c6c4408a6cff62d0d1f39c5b05accad95/Networking/4.%20Transmission%20Media/4.2%20-%20Wireless/4.2.6%20-%20Satellite.md), and thousands of routers screaming at each other to pass our WhatsApp meme.

---

## How is it different from LAN?

| Feature | LAN | WAN |
|--------|-----|-----|
| Range | Small (room, house, building) | Massive (worldwide) |
| Speed | Usually faster (local) | Slower (public & shared) |
| Ownership | You | ISPs, Telecom Giants |
| Complexity | Simple | Wildly complex |
| Cost | Cheap/Free | Expensive AF for companies |

---

## Who controls the WAN?

- **ISPs (Internet Service Providers)** — our Airtel, T-Mobile, etc.
- **Backbone providers** — think Level 3, Tata Communications, etc.
- **Routing gods** — BGP (Border Gateway Protocol) makes the magic happen

No single entity owns the whole WAN. It's like a bunch of old feudal lords agreeing not to fight (for now).

---

## What does WAN include?

- Our internet connection  
- The long-distance fiber routes under oceans  
- Satellite links and cellular towers  
- The big-ass routers connecting countries

Basically, if we’re accessing something **outside our LAN**, we’re in WAN territory.

---

## Real-world example

- Us: in Delhi
- Our cousin: in Armenia
- Our video call → travels through LAN → Router → ISP → WAN → cross-ocean fiber → WAN → ISP → Router → Cousin

Magical journey of light pulses, baby.

---

## ⚠️ Risks & Issues

- Latency — it’s going through 14 countries (probably)
- Censorship — some countries throttle or block traffic
- Congestion — traffic jams, but digital
- Surveillance — we are not alone ☠️

---

## How WAN is secured?

- [VPNs](https://github.com/bwbearr/Field-Notes/blob/11a39d8c6c4408a6cff62d0d1f39c5b05accad95/Networking/9.%20Security%20Concepts/VPN.md) to hide our stuff
- Encryption [(TLS/SSL)](https://github.com/bwbearr/Field-Notes/blob/11a39d8c6c4408a6cff62d0d1f39c5b05accad95/Networking/7.%20Protocols/7.6%20-%20Presentation%20Layer%20Protocols/TLS-SSL.md)
- Firewalls, [proxies](https://github.com/bwbearr/Field-Notes/blob/11a39d8c6c4408a6cff62d0d1f39c5b05accad95/Networking/9.%20Security%20Concepts/Proxy.md), routing policies
- Nation-state powers (or villains) 😶

---

## Sunmary

- WAN is like the **big internet highway**, while LAN is our home garage
- It connects cities, countries, and continents
- Owned by ISPs and telecom giants
- Slower, but massive and necessary
- Without WAN, we'd still be stuck emailing over LAN like it’s 1998

---

