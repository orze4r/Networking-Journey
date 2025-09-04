# ARP — "Hey, Who Has This IP?"

🗓️ M/Y: Jul-25  
📂 Category: Protocols

---

## What is ARP?

**ARP = Address Resolution Protocol**

ARP is like a **nosy neighbor** in a LAN:

> “I know your IP… but I don’t know where you live.  
> WHO has this IP? Please give me your MAC address!”

And boom — the device replies with its **MAC address**.

That’s what ARP does:  
**Finds the MAC address** of a device **when you only have its IP**.

---

## Why ARP Exists?

Because computers work on layers.

- **IP address** = where the device is logically (like its postal code)
- **MAC address** = actual hardware identity (like house number)

If I want to send something on a LAN, I **need the MAC**, not just the IP.

---

## Real Example:

My laptop wants to send data to `192.168.1.15`, but it doesn’t know the MAC.

It shouts on the network:

> “Who has 192.168.1.15? Tell me your MAC!”

If that device is active, it says:

> “Yo, that’s me — my MAC is AA:BB:CC:DD:EE:FF”

Then my laptop updates its ARP table and sends the frame directly to that MAC address.

---

## ARP Table

Every device keeps a mini-diary called the **ARP Table**, like:

| IP Address       | MAC Address           |
|------------------|-----------------------|
| 192.168.1.1      | AA:BB:CC:DD:EE:01     |
| 192.168.1.15     | AA:BB:CC:DD:EE:FF     |

## We can view it using:

| Bash       | OS/System           |
|------------------|-----------------------|
| arp -a      | Windows     |
| ip neigh     | Linux/Termux (Android)     |

---

## Summary of What It Does


| Thing       | What it Means           |
|------------------|-----------------------|
| ARP Request      | "Who has this IP?" (broadcasted)     |
| ARP Reply        | "That's me. Here's my MAC."     |
| ARP Table        | IP-to-MAC diary my system keeps |
| Purpose          | Allow devices to talk in LAN using MAC addresses |

---

## ARP Spoofing (Dark Side)

Some shady guy on your network can lie:

> “Hey! That IP? Yeah, that’s me. Send your data to me.”



Boom. You’re now the man in the middle.
This is how ARP spoofing or ARP poisoning works — used in LAN-based hacking.


---

## Can we Prevent ARP Attacks?

***Sort of.***

> **Use static ARP entries (manually set IP-MAC mappings)**

> **Use port security and VLANs**

> **Use tools like ARPwatch to monitor weird changes**

> **Use HTTPS (so even if someone spoofs, they can't decrypt)**


---

# Summary

**• ARP is used in LAN to resolve IP → MAC**

**• It works only inside local networks (not across the internet)**

**• Every device keeps an ARP table**

**• It can be abused (ARP spoofing)**

**• It’s like asking: “Who has this IP address? Give me your MAC!”**



---
