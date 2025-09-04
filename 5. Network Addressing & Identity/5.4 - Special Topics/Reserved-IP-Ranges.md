#  Reserved IP Address Ranges

🗓️ M/Y: Jul-25  
📂 Category: IP Addressing 

---

Some IP addresses are **not meant to be used publicly**. They're reserved for special purposes, internal use, testing, or legacy systems.

Let’s take a look:

---

### `127.0.0.0/8` — Loopback Range

- Used to test our own device (no actual network traffic).
- `127.0.0.1` is the famous one — a.k.a. `localhost`.

---

### `169.254.0.0/16` — APIPA

- Used when a device **can’t get IP from DHCP**.
- Auto-assigns itself a `169.254.x.x` IP to still talk to local devices.

---

### `10.0.0.0/8, 172.16.0.0–172.31.255.255, 192.168.0.0/16` — Private IP Ranges

- Meant for internal use only.
- Can’t be routed on the public internet.

---

### `0.0.0.0/8` — "This Network"

- Used in routing tables or boot processes to mean "unspecified host/network".

---

### `100.64.0.0/10` — Carrier-Grade NAT (CGNAT)

- Used by ISPs for NAT between customers and internet.
- Basically a **"middle ground"** private space.


---

### `224.0.0.0 – 239.255.255.255` — Multicast

- For sending a single packet to **multiple devices** at once.
- Used in streaming, routing protocols, etc.

---

###  `240.0.0.0/4` — Reserved for future use

- Not used in regular networks (yet).
- Reserved by IETF for possible future standards.

---

###  `255.255.255.255` — Broadcast Address

- "Shout to everyone" on the local network.
- Every device receives this.

---

### Key Reminder

These ranges **shouldn’t be used for normal host assignments** (unless explicitly needed).

---
