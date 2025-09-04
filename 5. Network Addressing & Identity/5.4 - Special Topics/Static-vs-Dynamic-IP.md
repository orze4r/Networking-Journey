# Static IP vs Dynamic IP Addresses

🗓️ M/Y: Jul-25  
📂 Category: IP Addressing 

---

## What’s an IP?
Think of it like our device's postal address on a network — without it, no one knows where to deliver data.

Now let’s talk about how this address gets assigned.

---

## Dynamic IP (Assigned Automatically)

Most of us use this daily — assigned automatically by the **DHCP server** (usually our router at home).

### Example:
- We connect to Wi-Fi.
- Router goes: "Here, take 192.168.1.23"
- We go: "Thanks, boss!"

**Dynamic IPs can change** (e.g., if we disconnect, reboot, or after a lease expires).

### ✅ Pros:
- Easy to use (no setup)
- Saves IPs by reusing
- Great for temporary devices

### ❌ Cons:
- IP changes often — not ideal for remote access
- Can cause issues in port forwarding or static routing

---

## Static IP (Manually set)

An IP **we assign ourselves** or **our router reserves for us**.

### Example:
- We set our IP as 192.168.1.100 manually.
- No matter how often we reconnect — we stay at that IP.

Used for:
- Servers
- Printers
- CCTV / NAS / Any device needing a **permanent** IP

### ✅ Pros:
- Always same IP
- Perfect for hosting services
- Great for troubleshooting

### ❌ Cons:
- Must avoid conflicts (like assigning the same IP for two different devices)
- Misconfig = network issues
- Tedious if too many devices

---

## Quick Demo

| Device        | Type       | IP Address         |
|---------------|------------|--------------------|
| Our Laptop    | Dynamic    | 192.168.1.21       |
| CCTV Camera   | Static     | 192.168.1.90       |
| File Server   | Static     | 192.168.1.99       |

---

## 🚀 Bonus: DHCP Reservation

Our router can **reserve** an IP for a device using its MAC address.
So, our device still gets an IP automatically — but it’s always the **same** one.

Best of both worlds!

---

> We can understand this deeper when we reach DHCP config and router-side network control.
