**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Heading:**
Ethernet Media Access Controller (EMAC)

**Subsection Heading:**
24.1 Overview

**Body Text:**

Features of Ethernet:
By using the external Ethernet PHY (physical layer), ESP32 can send and receive data via Ethernet MAC (Media Access Controller) according to the IEEE 802.3 standard, as Figure 24.1-1 shows. Ethernet is currently the most commonly used network protocol that controls how data is transmitted over local-and wide-area networks, abbreviated as LAN and WAN, respectively.

**Figure Caption:**
Figure 24.1-1. Ethernet MAC Functionality Overview

ESP32 MAC Ethernet complies with the following criteria:
- IEEE 802.3-2002 for Ethernet MAC
- Two industry-standard interfaces conforming with IEEE 802.3-2002: Media-Independent Interface (MII) and Reduced Media-Independent Interface (RMII).

**Subsection Heading:**
Features of MAC Layer

Supports:
- Support for a data transmission rate of 10 Mbit/s or 100 Mbit/s through an external PHY interface
- Communication with an external Fast Ethernet PHY through IEEE 802.3-compliant MII and RMII interfaces.

**List:**
- Carrier Sense Multiple Access / Collision Detection (CSMA/CD) protocol in half-duplex mode

**List:**
- IEEE 802.3x flow control in full-duplex mode
- operations in full-duplex mode, forwarding the received pause-control frame to the user application
- backpressure flow control in half-duplex mode

**Footer Information:**
Espressif Systems  
461 ESP32 TRM (Version 5.6)  

**Link Texts:**
Submit Documentation Feedback