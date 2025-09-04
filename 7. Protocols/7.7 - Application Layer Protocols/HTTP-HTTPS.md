# HTTP vs HTTPS

🗓️ M/Y: Jul-25  
📂 Category: Protocols

---

## What is HTTP?

**HTTP = HyperText Transfer Protocol**

It's the basic language our browser uses to talk to websites.

We type `http://example.com` → our browser sends a request → server replies with a webpage.

But… it’s not safe.

### The Problem with HTTP:

- No encryption.  
- Everything — our search, password, email — travels **in plain text**.  
- Anyone on the network (like your ISP, or a random guy on public WiFi) can spy on us.

---

## What is HTTPS?

**HTTPS = HTTP + Security** (the "S" stands for **Secure**)

It uses **TLS** (used to be called SSL) to **encrypt** the connection.

So now:
- No one can see what we're sending
- No one can tamper with our data
- Our browser verifies we're talking to the real website (not a fake one)

---

## Example

```text
http://example.com → Anyone can see everything  
https://example.com → All traffic is encrypted
```

---

## Real-World Analogy

| Situation  |	HTTP |	HTTPS |
|------------|-------|--------|
| Like       |	Sending a postcard |	Sending a sealed envelope |
| Visibility |	Everyone can read it |	Only receiver can read it |
| Protection |	None |	Encrypted and verified |
| Trust      |	Low |	High (verified with a certificate) |

---

## Cab we see the difference in browser?

Yes. Look at the URL bar:

> **http://** → ❌/⚠️ Insecure

> **https://** → ✅ Secure, usually shows a 🔒 padlock

---

## What makes HTTPS work?

- TLS (Transport Layer Security): Encrypts the data
- SSL Cert (really a TLS cert): Proves the site is legit
- Certificate Authority (CA): Issues the cert and signs it

 Our browser checks the certificate → if valid → secure connection starts.

---

## What HTTPS protects us from:

- Eavesdropping: Someone reading our data
- Tampering: Someone modifying what we're receiving
- Spoofing: Fake websites pretending to be real

---

## What HTTPS doesn’t do

- It doesn’t hide which website we’re visiting (just the content)
- It doesn’t make the website safe — just the connection
- It doesn’t stop tracking via cookies or browser fingerprinting

---

## HTTP vs HTTPS Table

| Feature |	HTTP |	HTTPS |
|---------|------|---------|
| Encryption |	❌ No |	✅ Yes |
| Data Protection |	❌ Visible to others | ✅ Encrypted end-to-end |
| Speed |	Slightly faster (but not anymore) |	Fast (with TLS 1.3) |
| Trust |	❌ Anyone can spoof |	✅ Verified identity |
| Padlock Icon |	❌ No padlock |	✅ Padlock shown in browser |
| SEO Ranking |	❌ Bad |	✅ Google prefers HTTPS |



---

## Overall

- HTTP is old and insecure.
- HTTPS encrypts traffic and proves site identity.
- Use HTTPS always — especially for logins, payments, or anything sensitive.

---

*⚠️ In 2025, if a website still only runs HTTP…
Either it's forgotten, sketchy, or we’re in a museum.*

