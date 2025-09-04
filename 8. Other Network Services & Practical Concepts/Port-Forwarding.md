# Port Forwarding

🗓️ M/Y: Jul-25  
📂 Category: Core Concepts  

---

## What is Port Forwarding?

Let’s say my PC at home is running a small game server on port 25565 (yes, Minecraft nerds).  
But someone on the internet wants to join it.

The problem? I’m behind a router.  
So when my friend tries to connect to my public IP, the router just shrugs:  
> “Who’s this port 25565 for?? Not my job lol”

**Port Forwarding** tells the router:  
> “Oi, if traffic comes to port 25565 — send it to THIS device inside the house.”

Boom. Problem solved. Router becomes my digital receptionist.

---

## What we're really doing

We are:
- Opening a specific **port** on our router
- Telling it to **forward incoming traffic** to a private IP inside our network
- Letting external traffic (internet) reach a device on LAN

---

## How It Works (Simple Visual)


```
🌐 Internet User
                       |
                       |  Request to: 49.x.x.x:8080
                       v
           ┌────────────────────────────┐
           │        Home Router         │  ← Public IP: 49.x.x.x
           │  (Port Forwarding Enabled) │
           └────────────────────────────┘
                       |
                       |  Forward to:
                       v
         ┌───────────────────────────────┐
         │  Local PC / Device            │  ← Private IP: 192.168.0.5
         │  Running App on Port: 8080    │
         └───────────────────────────────┘
                       |
                       |  Handles request
                       v
               🖥️ App / Service responds
```

The router is the middleman. It listens on a public port and forwards stuff to a private device.


---

## What we need to forward a port

- Our private IP (e.g. 192.168.1.5) — where the service is running
- The port number we want open (e.g. 8080, 22, 25565)
- Access to our router settings (192.168.0.1 usually)
- Option to add port forwarding rule (may be under "NAT", "Virtual Server", etc.)



---

## ⚠️ Gotchas

- If our ISP uses CGNAT, port forwarding will NOT work (we’re behind double NAT).
- If our firewall blocks the port, forwarding is useless.
- If our IP changes, rules break (unless static IP is used).
- Some ISPs block common ports (like 25 or 80) — for spam control.



---

## Is Port Forwarding safe?

- Not always. We’re opening a door into our network.
- If the service/app is insecure = attackers can use that port
- Always password-protect and secure the exposed service
- Don't forward unnecessary ports “just to test”



---

## Real World Examples

| Use Case	| Port Example |
|------------|--------------|
| Hosting a Minecraft server |	25565 |
| Remote SSH access | 22 |
| HTTP Web Server |	80 |
| CCTV or DVR access	| 8080 |
| Game consoles like PS/Xbox |	UPNP auto-handles these (usually) |



---

## Overall

- Port Forwarding = letting outside traffic reach an internal device
- Required when we want to host stuff from home
- Can be risky if done wrong
- Doesn’t work if we're behind CGNAT (mobile data, some ISPs)

---
