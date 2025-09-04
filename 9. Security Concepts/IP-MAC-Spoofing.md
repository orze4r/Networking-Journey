# IP & MAC Spoofing

🗓️ M/Y: Jul-25  
📂 Category: Protocols 

---

## What is spoofing?

**Spoofing = Faking something to trick the system.**  
In networking, it usually means pretending to be **someone else’s device** by copying their IP or MAC address.

Let’s break it into two:

---

## IP Spoofing

### What is it?

Changing our device’s **IP address** to impersonate another device or confuse the target.

### Why?

- To **bypass firewalls**  
- To **fool servers** into thinking we're trusted  
- Used in **DoS/DDoS attacks** (fake IP floods)
- Sneak past **IP-based filters**

### Real-World analogy:

We write our friend’s home address on a letter — so the receiver thinks it’s from them.

### But wait…

IP spoofing doesn’t help in 2-way comms much — because responses go to the **fake IP**, not us.

So it’s mostly used for:

- One-way attacks
- Confusing logs and tracking
- Recon in vulnerable networks

---

## MAC Spoofing

### What is it?

Faking the **MAC address** of our device — that’s the unique ID your network interface has.

Example:
```bash
Real MAC:     18:56:01:FA:00:AB  
Spoofed MAC:  00:11:22:33:44:55
```


### Why?

- Bypass **MAC filtering** on Wi-Fi networks
- Hide our identity on **LANs**
- **Impersonate** another device already trusted on the network
- Some public Wi-Fi or ISP services give **access based on MAC** — spoof to get in


### Real-World analogy:

We steal someone else’s uniform and sneak into their workplace pretending to be them.


---

## ⚠️ Legal & Ethical?

- Spoofing is not illegal by itself — but how we use it can land us in trouble.
- On our own network for learning = ✅
- To break into systems or spy on people = ❌ Big no-no

---

## How to protect against it

| Threat |	Defense Idea |
|--------|---------------|
| IP Spoofing |	Use firewalls with IP verification / filtering |
| MAC Spoofing |	Use port security (e.g., on switches), NAC |
| General |	Monitor logs, use intrusion detection systems |


---

## Tools people use (for education only)

- `macchanger` – for MAC spoofing (Linux)
- `ifconfig` / `ip` – change IP
- `nmap`, `ettercap`, etc – for sniffing/spoofing on LAN


---

## Overall

| Term         |	Spoofed What? |	Why It's Used                          |
|--------------|----------------|----------------------------------------|
| IP Spoofing  |	IP Address    | Hide identity, attack, bypass filters  |
| MAC Spoofing |	MAC Address   |	Bypass filters, trick networks         |



---

   *Gotta use it wisely or karma hits hard*
