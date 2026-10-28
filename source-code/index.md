Record \#511

# WPNForge Pro (v1.0.0)

Spacecraft Onboard Interface Services (SOIS) — High Data Rate Wireless Proximity Network (CCSDS 883.0-B-2)  
BLUE BOOK COMPLIANT

Proximity Nodes

3 Clients

Max Link Rate

600.4 Mbps

Path Loss (FSPL)

99.8 dB

Normative Audit

100%

## 

Proximity RF Controller

---

Proximity Client Entity Artemis xEMU Spacesuit Crew 1 (Wi-Fi 6 802.11ax) Lunar Terrain Vehicle (3GPP 5G NR / GWCN) Logistics Docking Chaser (Wi-Fi 6 802.11ax) EDCA Quality of Service (QoS) AC\_VO: Voice / Critical Telemetry (150 μs delay) AC\_VI: HD Video Streaming (450 μs delay) AC\_BE: Best Effort Commands (1,200 μs delay) AC\_BK: Background Bulk Telemetry (4,500 μs delay) Payload Size (Bytes) Evaluate Link & RF Budget Transmit Proximity Frame Test 3GPP GWCN Core Route Run CCSDS 883.0 Normative Audit

## 

Security & Encryption Parameters

---

Cipher Suite: WPA3-Enterprise 192-bit  
Encryption: GCMP-256 (Suite B)  
Key Exchange: EAP-TLS (ECDSA P-384 / SHA-384)  
Management Frames: Protected (PMF Mandatory)

## 

RF Link Budget & Physical Channel Metrics

---

Client: Artemis xEMU Spacesuit Crew 1 \[CLIENT\_EVA\_01\] Carrier Frequency: 5.18 GHz (Wi-Fi 6 UNII-1) Distance: 450.0 meters (EVA Spacesuit Envelope) Free Space Loss: 99.78 dB Received Power: \-66.78 dBm (EIRP Tx: 23 dBm, Rx Gain: 12 dBi) Signal-to-Noise: 32.22 dB SNR Modulation Scheme: MCS11 (1024-QAM 5/6) Channel Capacity: 600.4 Mbps (80 MHz Channel) Doppler Shift: 20.73 Hz (@ 1.2 m/s relative velocity)

## 

Wireless Proximity Telemetry & QoS Dispatch Log

---

\[INIT\] WPNForge Pro v1.0.0 Initialized. \[SOIS\] CCSDS 883.0-B-2 High Data Rate Wireless Proximity Network Engine Active. \[TOPOLOGY\] 3 Space Proximity Entities Registered (EVA, Surface Rover, Docking Chaser). \[QoS\] 4-Tier EDCA Prioritization Active (AC\_VO, AC\_VI, AC\_BE, AC\_BK). \[SECURITY\] WPA3-Enterprise 192-bit CNSA Suite B & 5G-AKA Mode Enabled.

## 

Normative Compliance Audit Matrix (CCSDS 883.0-B-2)

---

| Req ID | Clause | Requirement Name | Verified Specification Clause | Verdict   |
| :---- | :---- | :---- | :---- | :---- |
| WPN-001 | §2.2 | Operational Profile Conformance | IVW, EVA spacesuit, Surface, Orbital scopes | PASS |
| WPN-002 | §3.2 | IEEE 802.11ax Radio Stack | Wi-Fi 6 OFDMA & Target Wake Time | PASS |
| WPN-003 | §3.3 | 3GPP 5G NR Radio Stack | Release 17/18 Proximity Services (ProSe) | PASS |
| WPN-004 | §3.4 | 3GPP GWCN Architecture | Multi-operator PLMN shared radio access | PASS |
| WPN-005 | §4.2 | EDCA 4-Tier QoS Prioritization | AC\_VO, AC\_VI, AC\_BE, AC\_BK queues | PASS |

