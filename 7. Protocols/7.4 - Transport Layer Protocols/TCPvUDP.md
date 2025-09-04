# TCP vs UDP

🗓️ M/Y: Jul-25  
📂 Category: Protocols

---

## What are TCP and UDP?

These two protocols are like two ways of sending messages over the internet.  
Both ride on top of the IP layer, but they behave like two totally different personalities.

---

## What Is TCP?

**TCP = Transmission Control Protocol**

The “I-care-about-you” protocol.  
Reliable. Checks everything. Sends receipts. Won’t sleep until the message is delivered properly.

### What makes TCP reliable?

- **Connection-based** (like a phone call)
- **3-way handshake** before data transfer
- **Acknowledgment (ACK)** for every chunk
- **Resends if something is lost**
- Maintains **sequence/order**
- Slower, but **trustworthy**

### Real-World Examples:

- Loading a website (HTTP/HTTPS)
- Sending an email (SMTP)
- File transfers (FTP)
- Logging into remote systems (SSH)

### TCP Process (very simplified):

> **Client**: "Hey, you there?" → `SYN`  
> **Server**: "Yep, I’m here!" → `SYN-ACK`  
> **Client**: "Cool, let’s talk." → `ACK`  

✅ Connection is now established.  
📦 Data starts flowing, with `ACK`s confirming receipt.

(These SYN, ACK etc are TCP headers and flags. No need to learn unless going full network engineer mode lol)

**ACK** just means acknowledgement. Will study later when diving deeper into TCP.

---

## What is UDP?

**UDP = User Datagram Protocol**

The “idgaf” protocol.  
Sends data and doesn’t wait to see if it reached or not. No handshake, no drama.

### What makes UDP fast?

- **Connectionless**
- No handshakes
- No resending lost packets
- No guarantee of order
- **Fast AF** but risky

### Real-World Examples:

- Online gaming (CS:GO, Valorant, etc.)
- Video calls (Zoom, Meet)
- Streaming (Spotify, YouTube buffering)
- DNS lookups (even DNS runs over UDP most of the time)

---

## So when to use what?

| Feature         | TCP                               | UDP                            |
|-----------------|-----------------------------------|-------------------------------|
| Speed           | ❌ Slower (has to confirm stuff)  | ✅ Faster (just sends it)     |
| Reliability     | ✅ Yes                            | ❌ Nope                       |
| Ordered Data?   | ✅ Yes                            | ❌ No guarantees              |
| Suitable For    | Web, Email, SSH, FTP              | Games, Streaming, Calls       |

---

## Ports Example

- HTTP = **TCP port 80**
- HTTPS = **TCP port 443**
- DNS = **UDP port 53**
- VoIP = **UDP port 5060**
- SSH = **TCP port 22**

---

## Summary

- **TCP** is the control freak. Good for accuracy.
- **UDP** is the chill cousin. Good for speed.
- We’ll run into both. Must know what suits what.

---
