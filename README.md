# OSI Model Super Pack (No PDFs)

This repository is a **beginner-friendly, professional** guide to the **OSI Model** and how it’s used in real networks and cybersecurity.  
It explains **what the OSI model is**, **what each layer does**, **common protocols**, **device examples**, **security attacks by layer**, and a **step-by-step troubleshooting checklist**.

---

## What Is the OSI Model?

The **OSI Model (Open Systems Interconnection)** is a 7-layer framework that describes how data moves from one device to another across a network.

Think of it like **sending a package**:
- Your data goes through **7 steps** (layers)
- Each layer has a specific job
- If something breaks, the OSI model helps you pinpoint **where** the issue is happening

---

## The 7 OSI Layers (Top → Bottom)

### Layer 7 — Application  
**“The app you see.”**  
This is where apps communicate with the network.

**Examples**
- Web browser (Chrome, Edge)
- Email apps
- Netflix
- Discord

**Common protocols**
- **HTTP, HTTPS, FTP, DNS, SMTP**

**Easy analogy**
- Like the **post office front desk** where you hand over your package.

---

### Layer 6 — Presentation  
**“Makes data pretty and readable.”**  
This layer:
- Translates data (formats it)
- Encrypts/decrypts it (**SSL/TLS**)
- Compresses it (shrinks it)

**Examples**
- Encryption: **TLS/SSL**
- Formats: **JPEG, MP4, ASCII**

**Easy analogy**
- Like the worker who **wraps your package** so it’s secure and understandable anywhere.

---

### Layer 5 — Session  
**“Starts and ends conversations.”**  
This layer:
- Opens a connection
- Maintains it
- Closes it

**Examples**
- Logging into a website
- Keeping a video call open

**Easy analogy**
- Like a **phone call manager**:  
  “Hello?” → Start session  
  Talking → Maintain session  
  “Bye” → End session  

---

### Layer 4 — Transport  
**“Moves data and keeps it safe.”**  
Controls **how data moves** end-to-end.

**Two big protocols**
- **TCP** — Reliable, checks errors (like certified mail)
- **UDP** — Fast, no checking (like throwing a paper airplane)

**Key functions**
- Segmentation (break data into pieces)
- Flow control (don’t overwhelm the receiver)
- Error control (retransmit if needed)

**Easy analogy**
- The delivery truck deciding **careful vs fast** delivery.

---

### Layer 3 — Network  
**“Finds the best path.”**  
This is the **routing layer**.

**Jobs**
- Routing
- Logical addressing (**IP addresses**)
- Best path selection

**Common protocols**
- **IP**
- **ICMP** (ping)

**Easy analogy**
- Like the **GPS** choosing the best route.

---

### Layer 2 — Data Link  
**“Moves data inside a local network.”**  
Handles:
- **MAC addresses**
- Switching
- Frames
- Error detection (**CRC**)

**Common devices**
- **Switches**
- Bridges
- NICs (Network Interface Cards)

**Easy analogy**
- Like the **neighborhood roads** to reach the right house.

---

### Layer 1 — Physical  
**“The actual hardware.”**  
Everything that sends raw bits (1s and 0s):
- Cables
- Fiber optics
- Hubs
- Signals (electricity, light, radio waves)

**Easy analogy**
- The **road and wires** the delivery uses.

---

## Device Examples per OSI Layer (Quick Reference)

- **Layer 7 (Application):** Web servers, DNS servers, Email servers, Application servers  
- **Layer 6 (Presentation):** SSL/TLS accelerators, encryption appliances  
- **Layer 5 (Session):** VPN gateways, session controllers  
- **Layer 4 (Transport):** Firewalls, load balancers (port/connection aware)  
- **Layer 3 (Network):** Routers, Layer 3 switches  
- **Layer 2 (Data Link):** Switches, bridges, NICs, wireless APs (switching side)  
- **Layer 1 (Physical):** Cables, repeaters, hubs, fiber, Wi-Fi radio  

> Note: Some devices (especially modern security devices) can operate across multiple layers.

---

## Security Attacks by OSI Layer (Security+ Friendly)

- **Layer 7:** SQL Injection, XSS, CSRF, web app abuse  
- **Layer 6:** TLS/SSL downgrade attacks, weak encryption  
- **Layer 5:** Session hijacking, cookie/token theft, replay attacks  
- **Layer 4:** SYN floods, TCP reset attacks, some DDoS patterns  
- **Layer 3:** IP spoofing, routing manipulation, ICMP abuse (ping flood)  
- **Layer 2:** ARP poisoning, MAC flooding, VLAN hopping  
- **Layer 1:** Cable cuts, Wi-Fi jamming, physical tapping  

---

## Troubleshooting with the OSI Model (Simple Checklist)

Use this when “the network isn’t working”:

### 1) Layer 1 — Physical
- Check cables, Wi-Fi signal, power
- Check link lights on the NIC and switch
- Try a different cable/port

### 2) Layer 2 — Data Link
- Is the switch port up?
- Correct VLAN?
- Is the MAC address showing in the switch MAC table?

### 3) Layer 3 — Network
- Verify IP address, subnet mask, default gateway
- Ping the gateway and another host

### 4) Layer 4 — Transport
- Are the needed ports open?
- Is a firewall blocking TCP/UDP?
- Check active connections with tools like `netstat`

### 5) Layer 7 — Application
- Is the website/app itself down?
- Try another browser, device, or network

---

## OSI vs TCP/IP (How They Map)

The TCP/IP model has **4 layers**, but it covers the same idea:

- **OSI Layers 7–5 → TCP/IP Application**
- **OSI Layer 4 → TCP/IP Transport**
- **OSI Layer 3 → TCP/IP Internet**
- **OSI Layers 2–1 → TCP/IP Link**

---

## Easy Mnemonic (7 → 1)

**A**ll **P**eople **S**eem **T**o **N**eed **D**ata **P**rocessing  
(Application, Presentation, Session, Transport, Network, Data Link, Physical)

---

## Recommended Repository Structure

You can keep it simple:

```
osi-model-super-pack/
├─ README.md
└─ images/
   ├─ osi_chart.png
   └─ tcpip_chart.png
```

---

## License

Use this material for learning, labs, and portfolio documentation.  
(If you want a formal license file added, pick: MIT, Apache-2.0, or CC BY.)
