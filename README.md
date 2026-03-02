# Project 255 — Dual-Site Enterprise Network Design (Cisco Modeling Labs)

## Overview

**Project 255** is a small enterprise network design implemented using **Cisco Modeling Labs (CML)**.  
The topology consists of **five network devices** connecting two company office locations through an Internet Service Provider (ISP) while ensuring redundancy and centralized internet access.

The project demonstrates:

- Multi-site enterprise connectivity
- Redundant WAN links
- Centralized internet breakout
- Resource sharing between locations
- High availability design principles

---

## Network Topology

The company operates from two locations:

- **Headquarters (HQ)** — Accra
- **Branch Site** — Tamale

Both sites connect through a shared ISP infrastructure.

---

## Accra Headquarters (HQ)

The **Accra site** serves as the company's primary operational location and internet gateway.

### ISP Connectivity

The ISP provides **two WAN links** to ensure redundancy:

- **Primary Link:** Fiber Optic Connection
- **Secondary Link:** Microwave Radio Connection

### Key Characteristics

- Full internet access
- Centralized outbound traffic point
- Provides internet access for remote sites
- Acts as the enterprise edge network

---

## Tamale Branch Site

The **Tamale site** hosts the company’s **server farm**.

### Connectivity

Similar to the HQ, Tamale connects to the ISP using two redundant links:

- Fiber optic link
- Microwave radio backup link

### Key Characteristics

- Hosts internal company services
- No direct internet breakout
- Internet access routed through Accra HQ

---

## Interconnection Through ISP

The ISP network provides Layer 3 connectivity between both locations.

### Resource Sharing

The design allows:

- ✅ Accra users to access servers hosted in Tamale
- ✅ Tamale servers to reach the internet via Accra HQ
- ✅ Secure inter-site communication

---

## Traffic Flow Design

### Internet Access

All internet-bound traffic from Tamale is routed through the Accra headquarters.

### Server Access

HQ users can directly access enterprise services located in Tamale.

---

## Redundancy Strategy

Both locations implement link redundancy:

| Site   | Primary Link | Backup Link |
|--------|-------------|-------------|
| Accra  | Fiber       | Microwave   |
| Tamale | Fiber       | Microwave   |

Benefits include:

- Automatic failover capability
- Increased network uptime
- Improved reliability

---

## Design Objectives

The network was designed to achieve:

- High availability WAN connectivity
- Centralized security and internet control
- Efficient resource sharing
- Scalable enterprise architecture
- Realistic enterprise simulation in CML

---

## Devices Used

The lab consists of **five network devices**:

1. Accra Edge Router
2. Tamale Edge Router
3. ISP Core Router
4. Accra Internal Device
5. Tamale Server Network Device

---

## Technologies Demonstrated

- WAN redundancy
- Routed ISP interconnection
- Centralized internet gateway
- Enterprise traffic engineering
- Cisco Modeling Labs simulation

---

## Expected Outcomes

After implementation:

- Accra has direct internet connectivity.
- Tamale accesses the internet through Accra.
- Both sites communicate seamlessly.
- Network remains operational even if one WAN link fails.

---

## Conclusion

Project 255 demonstrates a practical enterprise network architecture using Cisco Modeling Labs.  
By combining redundant WAN links with centralized internet access, the design achieves reliability, scalability, and operational efficiency suitable for real-world deployments.

---

**Author:** Project 255 Lab  
**Platform:** Cisco Modeling Labs (CML)  
**Purpose:** Enterprise Network Design Simulation
