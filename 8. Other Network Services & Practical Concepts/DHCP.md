# DHCP — The Lazy Kid’s IP Dealer

🗓️ M/Y: Jul-25  
📂 Category: Core Concepts  

---

## What is DHCP?

**DHCP = Dynamic Host Configuration Protocol**

It’s the dude (or protocol) that gives out **IP addresses** to devices **automatically**, so we don’t have to do it manually.

Imagine entering a hotel:
> “Hey! I just arrived. Give me a room.”

The hotel (DHCP server) says:
> “Cool, here’s Room 101. Use it for the next 24 hours. Don’t trash it.”

Same thing. But replace "room" with **IP address**.

---

## Without DHCP?

We’d have to **manually assign IP addresses** to every device on our network.  
Not fun. Also a recipe for:

- IP conflicts (2 devices, same IP = disaster)
- Wasted time
- Chaos in large networks

---

## What DHCP gives us

It doesn’t just hand us an IP. It gives the the full starter pack:

| Thing              | Example               | Why it matters                |
|-------------------|-----------------------|-------------------------------|
| IP Address         | 192.168.1.24          | So our device can exist      |
| Subnet Mask        | 255.255.255.0         | So our device knows its LAN  |
| Default Gateway    | 192.168.1.1           | So our device can exit LAN   |
| DNS Server         | 8.8.8.8               | So our device can resolve domains |
| Lease Time         | 24 hours              | How long we keep that IP     |

---

## The 4-Step “DORA” Process (Yeah, like the Explorer)

DHCP works like a conversation. A 4-step convo, known as **DORA**:

| Step | What Happens                              |
|------|--------------------------------------------|
| **D**iscover | Client yells: "Is there any DHCP server here?" |
| **O**ffer    | Server replies: "Yo, I got an IP for you" |
| **R**equest  | Client says: "Okay, I’ll take it!"        |
| **A**ck      | Server says: "All yours. Lease starts now." |

This is all **broadcast** and **UDP-based** (port 67/68).

---

## Static IP vs Dynamic IP?

| Type        | Who Sets It?    | Good For                 | Example Use             |
|-------------|------------------|---------------------------|-------------------------|
| Static IP   | Us, manually    | Servers, Printers         | Always same IP          |
| Dynamic IP  | DHCP does it     | Normal devices, guests    | Different each time     |

---

## What if No DHCP?

- Our device sits with a **self-assigned IP** (like `169.254.x.x`)
- No internet
- We manually assign an IP (static)

---

##  How to Check DHCP & DNS on My Device?

- **Linux/Termux/Windows:**

| Command / Method              | OS / Tool        | What It Shows                        | Notes                                        |
|------------------------------|------------------|--------------------------------------|----------------------------------------------|
| `ipconfig /all`              | Windows (CMD)    | DHCP Enabled, DHCP Server, DNS       | Full adapter config, lease info too          |
| Control Panel → `ncpa.cpl`   | Windows (GUI)    | DHCP & DNS info                      | Via adapter → Status → Details               |
| `nslookup`                   | Windows (CMD)    | Current DNS resolver                 | Shows default DNS used for queries           |
| `cat /etc/resolv.conf`       | Linux            | DNS servers under `nameserver`       | Classic method                               |
| `resolvectl status`          | Linux (systemd)  | Per-interface DNS + DHCP info        | On distros using `systemd-resolved`          |
| `dhclient -v`                | Linux            | DHCP lease process & result          | Manually trigger DHCP and see lease info     |
| `ip a` or `ifconfig`         | Linux / Termux   | IP info (to infer DHCP use)          | Doesn’t directly say DHCP, but shows dynamic IP |
| `ip route`                   | Linux / Termux   | Default gateway (often DHCP server)  | Useful to trace route or DHCP gateway        |
| `getprop net.dns1`           | Termux (Android) | Shows DNS server assigned            | Usually set via DHCP from router             |
| `getprop dhcp.wlan0.server`  | Termux (Android) | Shows DHCP server IP                 | Replace `wlan0` with actual interface name    |


## DHCP Security?

- Anyone can spoof a DHCP server if your LAN is unprotected
- Rogue DHCP can assign fake gateways or DNS → Redirect all traffic (💀)


## Defense:
- Use port security, DHCP snooping, and don’t plug random devices into LANs.


---

## Overall

- DHCP gives IPs automatically.
- It works using a 4-step DORA process.
- Used in every normal home or office LAN setup.
- Without it, you need to assign IPs manually.
- Can be attacked via Rogue DHCP — so it’s not bulletproof.

---

