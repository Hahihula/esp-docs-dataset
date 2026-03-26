

# Chapter 52

## Ethernet Media Access Controller (EMAC)

### 52.1 Overview

By using the external Ethernet PHY (physical layer), ESP32-P4 can send and receive data via Ethernet MAC (Media Access Controller) according to the IEEE 802.3 standard, as Figure 52.1-1 shows. Ethernet is currently the most commonly used network protocol that controls how data is transmitted over local- and wide-area networks, abbreviated as LAN and WAN, respectively.

Figure 52.1-1. Ethernet MAC Functionality Overview

ESP32-P4 Ethernet MAC complies with the following standards:

*   IEEE 802.3-2002 for Ethernet MAC
*   IEEE 1588-2008 standard for precise networked clock synchronization
*   IEEE 802.3 standard Media Independent Interface (MII) and Reduced Media Independent Interface (RMII)
*   IEEE 802.3az-2010 for Energy Efficient Ethernet
*   IEEE 802.1Q for VLAN frame format

### 52.2 Features

*   Data rates of 10/100 Mbit/s through an external PHY interface
*   Communication with an external Fast Ethernet PHY through IEEE 802.3-compliant MII and RMII interfaces
*   Full-duplex and half-duplex modes