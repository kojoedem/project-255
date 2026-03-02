# Project 255 — Dual-Site Enterprise Network Design (Cisco Modeling Labs)

## Overview

**Project 255** is a small enterprise network design built using **Cisco Modeling Labs (CML)**.  
The project simulates a real-world company network connecting two geographically separated locations through an ISP while maintaining redundancy and centralized internet access.

The design demonstrates practical enterprise networking concepts including:

- Dual WAN redundancy
- Site-to-site connectivity
- Centralized internet breakout
- Server farm hosting
- High availability architecture

---

## 🌐 Network Topology

Below is the full Project 255 topology created in Cisco Modeling Labs.

![Project 255 Topology](project_255.png)

---

## Network Architecture

The company operates from two locations:

### 🏢 Accra — Headquarters (HQ)

Accra acts as the **primary internet gateway** for the organization.

#### ISP Connectivity

Two WAN links are provided:

- **Primary Link:** Fiber Optic
- **Secondary Link:** Microwave Radio (Backup)

#### Responsibilities

- Provides internet access
- Routes outbound traffic
- Allows Tamale servers to reach the internet
- Enterprise edge routing

---

### 🏭 Tamale — Branch Site (Server Farm)

The Tamale site hosts internal company services and applications.

Although connected to the ISP, it **does not directly access the internet**.  
All internet traffic is routed through the Accra headquarters.

#### Hosted Services

- ERP System
- Email Server 1
- Email Server 2
- Accounting Platform
- Social Platform

---

## 🔁 Traffic Flow Design

### Internet Access
Tamale → ISP → Accra HQ → Internet


### Server Access
Accra Users → ISP → Tamale Server Farm


---

## 🖥️ Server Services Verification

Below are screenshots showing each service running on different ports from the Tamale server network.

---

### ERP Service (Port 8001)

![ERP Service](erp.png)

---

### Email Server 1 (Port 8002)

![Email Server 1](email1.png)

---

### Email Server 2 (Port 8003)

![Email Server 2](email2.png)

---

### Accounting Service (Port 8004)

![Accounting Service](accounting.png)

---

### Social Platform (Port 8005)

![Social Platform](social.png)

---

## 🔄 Redundancy Strategy

| Site   | Primary Link | Backup Link |
|--------|-------------|-------------|
| Accra  | Fiber       | Microwave   |
| Tamale | Fiber       | Microwave   |

### Benefits

- Automatic failover capability
- Increased uptime
- Reliable enterprise connectivity

---

## 🧩 Devices Used

The lab consists of five main devices:

1. Accra Edge Router
2. Tamale Edge Router
3. ISP Core Router
4. Accra LAN Client
5. Tamale Server Network

---

## ⚙️ Technologies Demonstrated

- WAN Redundancy
- Inter-site Routing
- Centralized Internet Gateway
- Enterprise Network Simulation
- Cisco Modeling Labs (CML)

---

## ✅ Expected Outcome

After implementation:

- Accra has direct internet connectivity.
- Tamale accesses the internet via Accra.
- HQ users reach Tamale-hosted services.
- Network survives single WAN link failure.

---

## 📂 Full Project

Configurations and lab implementation are available in this repository.

---

## Conclusion

Project 255 demonstrates a practical enterprise network architecture using Cisco Modeling Labs.  
By combining redundant WAN links with centralized internet access, the design achieves reliability, scalability, and operational efficiency suitable for real-world deployments.

---
## Author

**Edem Ozone**  
Network Engineer | CML Lab Simulation  
Project 255 — Enterprise Network Design
