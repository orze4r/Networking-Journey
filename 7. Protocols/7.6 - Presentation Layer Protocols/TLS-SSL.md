# TLS vs SSL

🗓️ M/Y: Jul-25  
📂 Category: Protocols

---

## What are TLS and SSL?

Ever noticed websites start with **https://** instead of **http://**?

That’s because they’re using **TLS** (or previously, **SSL**) to keep our data encrypted and private.

In simple words:

> **HTTP = Talking loudly in public**  
> **HTTPS = Whispering in someone’s ear with noise-cancelling headphones**

---

## What is SSL?

- **SSL = Secure Sockets Layer**
- It was the OG technology to encrypt our browser’s communication with a website.
- Created in the 1990s. Had vulnerabilities.
- Versions: SSLv1 (never released), SSLv2, SSLv3 (all deprecated)

Basically, it’s dead. Don't use SSL. But people still say "SSL" out of habit.

---

## What is TLS?

- **TLS = Transport Layer Security**
- It replaced SSL.
- Stronger encryption, better privacy.
- Versions: TLS 1.0, 1.1, 1.2, and **1.3 (latest and best)**

If we’re using HTTPS today, we’re actually using **TLS**, not SSL.

---

## What does TLS do?

- Encrypts traffic between our browser and the server
- Prevents:
  - Hackers spying on our password
  - Data modification in transit
  - Impersonation (like fake websites)

Without TLS:
- Anyone in between (ISP, public WiFi guy, etc.) can see what we’re sending

---

## Real-World examples

| Site | Protocol |
|------|----------|
| http://example.com | No encryption |
| https://example.com | Uses TLS encryption (even if people say SSL) |

---

## How it works (simplified)

```text
Client (our browser) → "Hey server, let's talk securely!"
Server → "Sure, here's my certificate"
Client → "Looks valid. Let's agree on a secure key"
🔐 They agree and start encrypted comms 🔐
```

This is called a TLS Handshake.


---

## SSL vs TLS: What's the difference?

| Feature          |	SSL                   |	TLS                        |
|------------------|------------------------|----------------------------|
| Status           |	Deprecated ❌       	| Actively used ✅           |
| Security         |	Weak & broken         |	Strong encryption          |
| Speed            |	Slower handshake      |	Faster, better optimized   |
| Support          |	Not supported anymore |	Widely supported           |


---

# Common Misconceptions

- "SSL certificate" = actually TLS certificate now
- SSL is not used anymore in secure websites
- VPN ≠ TLS (though TLS is used inside some VPN protocols)


---

## Certificate Authority (CA)?

Websites need a certificate to prove they are legit.
This cert is issued by a CA (Certificate Authority) like Let’s Encrypt, DigiCert, etc.
Our browser checks the cert during handshake.

---

## Summary

- SSL is dead. TLS is the real deal.
- HTTPS websites use TLS to encrypt our connection.
- It protects our data from being sniffed, modified, or intercepted.
- TLS 1.3 is latest and best.
- “SSL Certificate” is just an old name. It’s really TLS.

---

 Encryption isn't a luxury. It's the default now. If a site is still HTTP-only, maybe... don’t trust it.
