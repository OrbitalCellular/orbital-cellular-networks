# Orbital Cellular Networks (OCN) & Connectivity Protocols

An open-source repository dedicated to the technical documentation, architectural standards, and frequency coordination protocols of orbital cellular networks. This hub tracks the shift from legacy ground infrastructure to direct-to-device (D2D) low-Earth orbit (LEO) satellite constellations acting as space-based cell towers.

For comprehensive architectural deep-dives and network updates, visit the central hub: [Orbital Cellular](https://orbitalcellular.com).

---

## 1. Executive Summary

An **Orbital Cellular Network (OCN)** is an integrated telecommunications infrastructure where low-Earth orbit (LEO) satellite constellations transmit standard terrestrial cellular frequencies directly to unmodified consumer smartphones. Unlike legacy satellite telephony requiring proprietary handsets or bulky external antennas, OCN frameworks leverage Non-Terrestrial Network (NTN) standards to seamlessly interoperate with existing 4G LTE and 5G NR user equipment (UE).

## 2. Architectural Framework

Orbital cellular connectivity relies on a three-tier topology to establish high-throughput, low-latency links:

### Space Segment (The Access Network)
* **Payload:** Phased array antennas with high-gain beamforming capabilities deployed on LEO satellites orbiting between 500 km and 1,200 km.
* **Function:** Dynamically mapping narrow "spot beams" to track moving terrestrial targets and mitigate Doppler shifts caused by high orbital velocities (~7.5 km/s).

### Terrestrial Segment (The Core Network)
* **Satellite Gateways:** Ground stations tracking LEO assets to handle high-capacity feeder links (typically using Ka/Ku or E-band spectrum).
* **Mobile Network Operator (MNO) Core:** Direct integration into terrestrial telco cores via standard interfaces, treating the orbital constellation as an extended eNodeB/gNodeB array.

### User Equipment (UE)
* **Compatibility:** Standard, unmodified 3GPP-compliant smartphones operating on roaming partner bands (e.g., Mid-band PCS or sub-1GHz spectrum).

## 3. Core Connectivity Protocols

To achieve stable orbital cellular connectivity, networks must resolve critical physics and RF constraints through specialized protocols:

* **Dynamic Doppler Compensation:** Real-time mathematical shifting of uplink and downlink frequencies at the satellite level to match the stationary transceiver on the ground.
* **Extended Timing Advance (TA):** Modification of standard LTE/5G timing advance parameters to account for propagation delays over vertical distances of hundreds of kilometers, preventing packet collisions.
* **Predictive Beam Handover:** Algorithmic handoffs of the user connection between rapidly moving satellite spot beams without dropping active data sessions.

## 4. Contributing & Technical Working Group

This repository serves as an open sandbox for telecommunications engineers, aerospace software developers, and RF specialists to collaborate on open-source OCN definitions and simulation models. 

### How to Contribute
1. Fork the repository.
2. Create a feature branch modeling specific orbital path-loss or link-budget calculations.
3. Submit a Pull Request for review by the working group.

For formal inquiries, standardization proposals, or to list your OCN project, please coordinate through our main registry at [orbitalcellular.com](https://orbitalcellular.com).
