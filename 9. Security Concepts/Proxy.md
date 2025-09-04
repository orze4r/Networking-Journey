# Proxy

🗓️ M/Y: Jul-25  
📂 Category: Core Concepts  

---

## What even is a Proxy?

**Proxy = Middleman server between me and the internet.**

Think of it like this:  
Me → Proxy → Internet

The website I visit doesn’t talk to *me* directly — it talks to the proxy.  
The proxy passes the message back and forth like a sketchy postman who hides my return address.

---

## What does a Proxy do?

✅ Hides my **real IP** from websites  
✅ Lets me **bypass censorship** or firewalls  
✅ Can **filter traffic** (like in schools or offices)  
✅ Used to **cache** content (speed up repeated access)

---

## But how is this different from VPN?

| Feature | VPN | Proxy |
|--------|-----|-------|
| IP Hidden | ✅ Yes | ✅ Yes |
| Encrypts Traffic | ✅ Full Encryption | ❌ Usually No |
| Works on OS Level | ✅ Yes (entire device) | ❌ App/browser only |
| Slower/Faster | Slightly Slower (due to encryption) | Faster but less secure |
| Good for Privacy? | ✅ Strong | ⚠️ Weak-ish |

So yeah — proxies are mostly **for convenience**, not real privacy.

---

##  Types of Proxies

### 🔹 HTTP Proxy  
- Works only for websites (HTTP traffic)  
- Doesn’t encrypt  
- Good for browsing anonymously (basic)

### 🔹 SOCKS Proxy  
- Works with any traffic (games, torrents, etc)  
- Slower, but more flexible  
- SOCKS5 = most used today

### 🔹 Transparent Proxy  
- We don’t even know it’s there  
- Used by schools, cafés, etc to filter/block stuff  
- It doesn’t hide IP, just intercepts traffic

---

## So why would anyone use Proxy?

- To **change location/IP** quickly  
- To **bypass blocks** at school or work  
- To **scrape data** (bots use proxies like oxygen)
- To avoid **basic IP bans**

But again — **no encryption**, so it’s NOT for handling private stuff.

---

## ⚠️ Major Gotchas

- ❗ My ISP *can still see* my activity  
- ❗ The proxy server can see my data (unless HTTPS)  
- ❗ Not for security — anyone sniffing my connection can read the traffic  
- ❗ Not all apps support proxies

---

## Real World Use

- Browsers: Firefox lets us set proxy manually  
- Android: Some apps let us set proxy per-app  
- Scraping: Use rotating proxies (free/paid) to avoid bans  
- Tools: curl, proxychains, torify, etc. can use proxies

---

## Overall

**Proxy = traffic middleman.**  
Great for bypassing blocks and hiding IPs…  
…but terrible if I'm looking for encryption, privacy, or true anonymity.

Use it when you need something *quick, dirty, and low-stakes.*

---
