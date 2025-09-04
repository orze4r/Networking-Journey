# SAN (Storage Area Network)

🗓️ M/Y: Jul-25  
📂 Category: Network Types - Wide or Specialized Networks

---

## 💾 What is a SAN?

**SAN = Storage Area Network**  
A SAN is a **dedicated high-speed network** built purely for **data storage**. Not for memes, not for Zoom calls — just **raw storage access**.

It connects **servers** to **shared storage devices** (like disk arrays, SSD/NVMe racks, or tape libraries) over a separate network infrastructure.

---

## Where SANs are used?

- Enterprise data centers  
- Cloud providers (AWS, Azure backend)  
- Banks and financial institutions  
- Video editing or scientific workloads  
- Backup and disaster recovery zones

Basically anywhere that storage demands are **huge**, and speed + reliability are critical.

---

## How does a SAN work?

- SAN separates **storage traffic** from our main LAN
- Uses **Fiber Channel (FC)** or **iSCSI** protocols
- Devices access storage **as if it's locally attached**, but it's over a remote network

> Think of SAN like a magical remote hard drive that's faster than most local drives 🪄

---

## Why use a SAN?

| Reason            | Meaning                                            |
|-------------------|----------------------------------------------------|
| Performance       | High-speed connections — not limited by LAN speed |
| Scalability       | Add more storage without touching each server     |
| Centralization    | One storage pool for many servers/apps            |
| Reliability       | Redundant links, RAID arrays, backups             |

---

## Tech used in SAN

- **Fibre Channel (FC)** — dedicated hardware, expensive but fast
- **iSCSI** — Internet Small Computer System Interface (uses IP)
- **SAS** / **NVMe-oF** — used inside storage nodes
- **Storage arrays**, **RAID controllers**, **HBAs (host bus adapters)**

---

##  What SAN is NOT:

- ❌ It’s NOT our regular network file sharing (that’s NAS)
- ❌ It’s not for random users — it’s for servers, DBs, enterprise software

---

## Overall

- There is difference between NAS (file level) and SAN (block level)
- SAN is for fast, direct, professional-grade storage — not media streaming
- It’s a different beast with different protocols and hardware

---
