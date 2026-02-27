# 🌐 Computer Networks — Assignment 1
### Network Topology Analysis using Cisco Packet Tracer

![University](https://img.shields.io/badge/University-K.R%20Mangalam-blue?style=flat-square)
![Program](https://img.shields.io/badge/Program-B.Tech%20CSE%20(AI%26ML)-green?style=flat-square)
![Subject](https://img.shields.io/badge/Subject%20Code-ENCS304-orange?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

---

## 👤 Student Details

| Field | Details |
|---|---|
| **Name** | Rudraraj Radhwani |
| **Roll No.** | 2401731349 |
| **Subject** | Computer Networks (ENCS304) |
| **Submitted To** | Mr. Aijaz Mohammed |
| **Institution** | K.R Mangalam University, SOET |

---

## 📋 Overview

This assignment explores three fundamental **network topologies** — Star, Bus, and Ring — simulated using **Cisco Packet Tracer**. Each topology was tested for communication behavior, collision handling, and fault tolerance.

---

## 🔬 Experiments

### ⭐ Task 1 — Star Topology (Switch-based)

> **Device Used:** Cisco 2950 Switch

**Setup:** 4 PCs (PC0–PC3) connected to a central switch.

**Observation:**
- When PC0 pings PC1, the switch learns MAC addresses and forwards traffic **only** to PC1.
- PC2 and PC3 **do not receive** the ICMP packets.
- Switch creates **separate collision domains** per port — no collisions occur.

---

### 🚌 Task 2 — Bus Topology (Hub-based)

> **Device Used:** Hub-PT

**Setup:** 4 PCs (PC0–PC3) connected to a central hub.

**Observation:**
- Hub broadcasts all traffic to **every connected device**.
- All PCs share a **single collision domain**.
- Simultaneous transmissions cause **collisions** (visible as fire/explosion icons in Packet Tracer).

---

### 💍 Task 3 — Ring Topology (Redundant Switch Layout)

> **Device Used:** Multiple Cisco 2960 Switches

**Setup:** Switches interconnected in a ring, with PCs attached to each switch.

**Observation:**
- **Spanning Tree Protocol (STP)** automatically blocks one port (shown in orange) to prevent logical loops.
- Traffic is routed efficiently while redundancy is maintained in the background.

---

### 🔥 Task 4 — Failure Test (Fault Tolerance)

**Setup:** A direct link between two switches in the ring is deliberately disconnected.

**Observation:**
- Initial ICMP ping **fails** as the primary path is broken.
- STP detects the failure and transitions the blocked (orange) port to **forwarding (green)**.
- Network **self-heals** — communication is restored **without manual reconfiguration**.
- Proves that redundant topologies prevent total network collapse.

---

## 📊 Topology Comparison

| Feature | Star (Switch) | Bus (Hub) | Ring (Redundant) |
|---|---|---|---|
| **Central Device** | Switch | Hub | Multiple Switches |
| **Collision Domain** | Per port (isolated) | Single shared | Per port (isolated) |
| **Fault Tolerance** | ❌ Single point of failure | ❌ Hub failure = total loss | ✅ STP self-heals |
| **Traffic Efficiency** | ✅ Unicast forwarding | ❌ Broadcasts to all | ✅ Directed routing |
| **Scalability** | ✅ High | ❌ Low | ✅ Medium-High |

---

## 🧠 Conclusion

> Star topologies provide **efficient, collision-free communication** via intelligent switching, but have a **single point of failure**.  
> Ring-like layouts with **redundant links** allow the network to *self-heal* using STP when a primary cable fails.  
> Choosing the right topology requires balancing **hardware costs** against the need for **high availability and performance**.

---

## 🛠️ Tools Used

- **Cisco Packet Tracer** — Network simulation
- **ICMP Ping** — Connectivity testing
- **Spanning Tree Protocol (STP)** — Loop prevention & fault recovery

---

*Assignment submitted as part of B.Tech CSE (AI&ML) — ENCS304 Computer Networks, K.R Mangalam University*
