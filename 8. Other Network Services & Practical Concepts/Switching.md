# Switching — Local Data Doing Gymnastics

🗓️ M/Y: Jul-25  
📂 Category: Core Concepts  

---

## What is Switching?

Routing is for **getting data across networks**.  
**Switching** is for **getting data across devices inside your own network (LAN)**.

Basically:

> Me and my friends are in one big room (your LAN).  
> I yell “Pass the ball to Ravi!”  
> The switch hears it and throws the ball directly to Ravi.  
> No one else gets disturbed.

That’s switching.

---

## Where It Happens?

Inside a **LAN (Local Area Network)**:  
- My home  
- Office  
- Café  
- Gaming setup  
Anywhere devices are connected to a **network switch** (or router with built-in switching).

---

## Who Does the Switching?

A **network switch** — it’s like the local traffic cop in your LAN.

It makes sure:
- The **printer** gets print requests
- My annoying **smart TV** gets YouTube from your phone
- My **laptop** talks to my PC for file sharing

---

## MAC Addresses, Not IPs

Switches don’t care about IP addresses.

They use **MAC addresses** (unique physical addresses of devices).

Switch builds a **MAC address table** like:

| MAC Address         | Port |
|---------------------|------|
| AA:BB:CC:DD:EE:01    | 1    |
| AA:BB:CC:DD:EE:02    | 2    |
| AA:BB:CC:DD:EE:03    | 3    |

So if device on Port 1 wants to talk to device on Port 2 — it sends the frame, switch checks the table, and sends it to Port 2 only. Neat.

---

## 📦 Switching = Fast local delivery

Switching sends **Ethernet frames** — not IP packets.

We say:
> “Yo switch, give this to whoever has MAC:AA:BB:CC.”

It says:
> “On it, boss.”

Fast. Direct. Efficient. No round-trips to the ISP.

---

## ⚙️ Types of Switching (We may or may not need this yet)

| Type          | What It Means                           |
|---------------|------------------------------------------|
| **Circuit**   | Old-school telephony, not used in LANs   |
| **Packet**    | Most common, especially in IP networks   |
| **Frame**     | Used by Ethernet switches in LANs        |

---

## Learning so far

- Switching = local LAN communication  
- Uses **MAC addresses**  
- Switch builds a table to know “who is where”  
- Doesn’t flood the network unless it doesn’t know where to send  
- Faster than routing — because it's local and direct

---

## What’s NOT Switching?

- Switch ≠ Hub (hubs blast data to everyone like drunk DJs)
- Switch ≠ Router (routers care about IPs and wide-area traffic)

---

## 🔒 Is Switching secure?

Not by default.  
Anyone on my LAN can sniff frames if not protected (e.g., via port security or VLANs).

Also: **ARP spoofing** can trick switches — that’s how LAN-based attacks happen.

---

## Summary

- Switches manage **LAN communication**  
- Use **MAC address tables**  
- Local, fast, and efficient  
- Way better than dumb hubs  
- Not the same thing as routers

---
