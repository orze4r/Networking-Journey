# Network vs Broadcast Address

🗓️ M/Y: Jul-25  
📂 Category: IP Addressing 

---

When we divide an IP block (subnetting), **two special IPs** in every range are **reserved**:
1. One to identify the **network itself**
2. One to **message all devices** in that network

Let’s break them down:

---

## Network Address

The **first IP** in any subnet range. It doesn't go to any device — it just represents the **entire network**.

- Think of it like the *name* of a group, not a person in it.
- We can’t assign this to a computer, router, or phone.

### Example:
For the subnet `192.168.10.0/24`:
- Subnet range: `192.168.10.0` to `192.168.10.255`
- `192.168.10.0` = **Network Address**

It means: “This is the 192.168.10.x network block.”

---

## Broadcast Address

The **last IP** in the subnet. It’s used to **send messages to ALL devices** inside the subnet at once.

-  Think of it as “shouting to everyone in the room.”
-  We also can’t assign this to any device.

### Example:
Same block: `192.168.10.0/24`  
- `192.168.10.255` = **Broadcast Address**

Used by devices when they want to say:  
> “Hey, everyone on this network — listen up!”

---

## How to calculate them

### CIDR: `/24` = 255.255.255.0  
- Subnet block size = 256 addresses  
- → First address = **Network**  
- → Last address = **Broadcast**  
- → Usable addresses = Between them (from `.1` to `.254`)

So:

Network:   192.168.10.0
Usable:    192.168.10.1 to 192.168.10.254
Broadcast: 192.168.10.255

---

### One more example: `/26` = 255.255.255.192  
- Block size = 64 addresses  
→ Range: `192.168.1.64` to `192.168.1.127`

Network:   192.168.1.64
Usable:    192.168.1.65 to 192.168.1.126
Broadcast: 192.168.1.127

---

## Why it matters

- Don’t assign devices to `.0` or `.255` (or whatever our first/last IP is)
- Helps in calculating usable host IPs when subnetting
- Important in troubleshooting, routing, and firewall setups

---

> 🚀 Just remember: **first = Network**, **last = Broadcast**  
> Everything in between = **usable IPs**


---
