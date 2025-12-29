# OSI Model for Cybersecurity – Concepts, Devices, Attacks & Troubleshooting

In-depth OSI model reference detailing layer-by-layer functions, protocol behavior, device mapping, security attack vectors by layer, and structured troubleshooting methodology. Built to demonstrate practical networking knowledge and analytical understanding of layered network architecture.

---

## What Is the OSI Model?

The **OSI Model (Open Systems Interconnection)** is a 7-layer framework that describes how data moves from one device to another across a network.

Think of it like **sending a package**:
- Your data goes through **7 steps** (layers)
- Each layer has a specific job
- If something breaks, the OSI model helps you pinpoint **where** the issue is happening


<img width="1080" height="1080" alt="image" src="https://github.com/user-attachments/assets/1b250d64-ef6a-4931-9898-b6d7f6c5f98e" />

---

## The 7 OSI Layers

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


<img width="516" height="430" alt="image" src="https://github.com/user-attachments/assets/bf3d3c47-2ed2-4377-b5fc-a4fb10efc558" />


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


<img width="516" height="430" alt="image" src="https://github.com/user-attachments/assets/f3e2d823-c36b-449a-93f1-0505026687f1" />


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


<img width="516" height="430" alt="image" src="https://github.com/user-attachments/assets/1f64dbe0-7b0f-4698-8013-7ec0a5066866" />


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


<img width="516" height="430" alt="image" src="https://github.com/user-attachments/assets/335c95b2-2012-4328-b9ac-f8b1370e1b02" />


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


<img width="516" height="430" alt="image" src="https://github.com/user-attachments/assets/efbe8a03-669e-48ed-96ff-c372ee5d206c" />


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


<img width="516" height="430" alt="image" src="https://github.com/user-attachments/assets/a5553ed2-3c79-4ebf-8a22-3f1c9897a740" />

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


<img width="516" height="430" alt="image" src="https://github.com/user-attachments/assets/d043ce7b-9863-4f16-9e56-497f80ed5cd9" />


---

## Device Examples per OSI Layer

- **Layer 7 (Application):** Web servers, DNS servers, Email servers, Application servers  
- **Layer 6 (Presentation):** SSL/TLS accelerators, encryption appliances  
- **Layer 5 (Session):** VPN gateways, session controllers  
- **Layer 4 (Transport):** Firewalls, load balancers (port/connection aware)  
- **Layer 3 (Network):** Routers, Layer 3 switches  
- **Layer 2 (Data Link):** Switches, bridges, NICs, wireless APs (switching side)  
- **Layer 1 (Physical):** Cables, repeaters, hubs, fiber, Wi-Fi radio  

> Note: Some devices (especially modern security devices) can operate across multiple layers.

---

## Security Attacks by OSI Layer

- **Layer 7:** SQL Injection, XSS, CSRF, web app abuse  
- **Layer 6:** TLS/SSL downgrade attacks, weak encryption  
- **Layer 5:** Session hijacking, cookie/token theft, replay attacks  
- **Layer 4:** SYN floods, TCP reset attacks, some DDoS patterns  
- **Layer 3:** IP spoofing, routing manipulation, ICMP abuse (ping flood)  
- **Layer 2:** ARP poisoning, MAC flooding, VLAN hopping  
- **Layer 1:** Cable cuts, Wi-Fi jamming, physical tapping  


<img width="1536" height="1024" alt="ChatGPT Image Dec 29, 2025, 03_12_09 PM" src="https://github.com/user-attachments/assets/ca29d1e4-c731-47a7-bfb8-2a61fd604c1e" />

---

## Troubleshooting with the OSI Model

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


<img width="1536" height="1024" alt="ChatGPT Image Dec 29, 2025, 03_10_42 PM" src="https://github.com/user-attachments/assets/e1cef0c7-22f5-48b6-b018-8a994075b811" />

---

## OSI vs TCP/IP

The TCP/IP model has **4 layers**, but it covers the same idea:

- **OSI Layers 7–5 → TCP/IP Application**
- **OSI Layer 4 → TCP/IP Transport**
- **OSI Layer 3 → TCP/IP Internet**
- **OSI Layers 2–1 → TCP/IP Link**



<img width="1080" height="1350" alt="image" src="https://github.com/user-attachments/assets/38247f65-1c32-4b71-983a-9a96d8754fdf" />


---

