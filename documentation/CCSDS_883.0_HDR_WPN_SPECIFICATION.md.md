# CCSDS 883.0-B-2 High Data Rate Wireless Proximity Network Communications (HDR-WPN) Engineering Specification

## 1\. Executive Summary & Purpose

The **High Data Rate Wireless Proximity Network Communications (HDR-WPN)** standard defined in **CCSDS 883.0-B-2 (Blue Book, Issue 2, May 2024\)** establishes a unified, multi-gigabit wireless communications architecture for space mission proximity networks.

It defines physical layer parameters, medium access control (MAC), Quality of Service (QoS), security suites, and cellular core gateway capabilities across:

- **Intra-Vehicular Wireless (IVW)**: In-cabin wireless avionics, wearable biomedical sensors, and crew handheld devices.  
- **Extra-Vehicular Activity (EVA)**: Astronaut spacesuit telemetry, real-time biometrics, and 4K/HD helmet video streams.  
- **Surface Proximity**: Lunar and Martian surface links connecting landers, pressurized rovers, autonomous robotic platforms, and habitats.  
- **Orbital Proximity**: On-orbit satellite servicing, rendezvous, and docking chaser telemetry.

---

## 2\. Dual-Stack Radio Architecture (§3.2, §3.3)

CCSDS 883.0-B-2 standardizes two complementary wireless radio stacks:

### 2.1 IEEE 802.11 (Wi-Fi 6 / 802.11ax & Wi-Fi 5 / 802.11ac)

- **OFDMA & MU-MIMO**: Orthogonal Frequency-Division Multiple Access allowing simultaneous multi-user telemetry and video streaming without channel collision.  
- **Modulation**: High-order modulation up to 1024-QAM (MCS11) providing throughput exceeding 600 Mbps in 80 MHz channel widths.  
- **Power Conservation**: Target Wake Time (TWT) scheduling minimizing battery drain on wearable EVA biosensors.

### 2.2 3GPP Cellular (5G NR Release 17/18 & LTE)

- **3GPP Gateway Core Network (GWCN) Architecture (§3.4)**: Standardizes shared Radio Access Network (RAN) infrastructure allowing multiple international space agency core networks (e.g. NASA PLMN `001-01`, ESA PLMN `001-02`, JAXA PLMN `001-03`) to connect through a single lunar surface gNB base station.  
- **Proximity Services (ProSe)**: Sidelink direct device-to-device communications without core network backhaul dependencies.

---

## 3\. Cryptographic Security Subsystem (§5.2)

- **WPA3-Enterprise 192-bit Security Mode**: Implements Commercial National Security Algorithm (CNSA / Suite B-192) cryptography:  
  - Encryption: 256-bit Galois/Counter Mode Protocol (GCMP-256).  
  - Key Exchange: Extensible Authentication Protocol with Transport Layer Security (EAP-TLS) using Elliptic Curve ECDSA P-384 and SHA-384 message digests.  
  - Management Frames: Protected Management Frames (PMF / 802.11w) mandatory to prevent deauthentication spoofing.

---

## 4\. Enhanced Distributed Channel Access (EDCA) QoS (§4.2)

Traffic is strictly classified into four priority access categories:

1. **`AC_VO` (Voice / Critical Telemetry)**: CWmin=3, CWmax=7, AIFSN=2 (Sub-millisecond transit delay).  
2. **`AC_VI` (HD Video Streaming)**: CWmin=7, CWmax=15, AIFSN=2 (Spacesuit helmet cameras and inspection feeds).  
3. **`AC_BE` (Best Effort Commands)**: CWmin=15, CWmax=1023, AIFSN=3 (Routine telecommands and flight scripts).  
4. **`AC_BK` (Background Bulk Telemetry)**: CWmin=15, CWmax=1023, AIFSN=7 (Scientific datasets and delayed logs).