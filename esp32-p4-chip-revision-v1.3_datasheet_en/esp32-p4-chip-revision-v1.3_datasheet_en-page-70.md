**4 Functional Description**

- Programming the chip's flash
- CPU debugging with compact JTAG instructions
- A full-speed USB PHY integrated in the chip
- Two integrated full-speed transceivers
- Choosing from two full-speed integrated transceivers GPIO24/GPIO25 and GPIO26/GPIO27. The USB Serial/JTAG Controller interface can use each of them.
- Supporting USB 2.0 OTG using one of the integrated transceivers while USB Serial/JTAG using the other one

**Pin Assignment**

The pins connected to D+ and D- signals for two pairs of USB PHY are multiplexed with GPIO24–GPIO25 and GPIO26–GPIO27. The USB Serial/JTAG Controller interface can use each of them. By default, the pins are multiplexed with GPIO24–GPIO25.

**4.2.12 Ethernet Media Access Controller (EMAC)**

By using the external Ethernet PHY (physical layer), ESP32-P4 can send and receive data via Ethernet MAC (Media Access Controller) according to the IEEE 802.3 standard.
ESP32-P4 Ethernet MAC complies with the following standards:
- IEEE 802.3-2002 for Ethernet MAC
- IEEE 1588-2008 standard for precise networked clock synchronization
- IEEE 802.3 standard Media Independent Interface (MII) and Reduced Media Independent Interface (RMII)
- IEEE 802.3az-2010 for Energy Efficient Ethernet
- IEEE 802.1Q for VLAN frame format

**Feature List**

- Data rates of 10/100 Mbit/s through an external PHY interface
- Communication with an external Fast Ethernet PHY through IEEE 802.3-compliant MII or RMII interface (only one can be used at a time)
- Full-duplex and half-duplex modes:
  - Carrier Sense Multiple Access or Collision Detection (CSMA/CD) protocol in half-duplex mode
  - IEEE 802.3x flow control in full-duplex mode
  - Optional forwarding of received pause control frame to the user application in full-duplex mode
- Back-pressure flow control in half-duplex mode
- Automatic transmission of zero-quanta pause frame on deassertion of flow control input in full-duplex mode

- Preamble and start-of-frame data (SFD) insertion in Transmit, and deletion in Receive paths

**Footer**

Espressif Systems  
70  
[Submit Documentation Feedback](#)  
ESP32-P4 Series Datasheet v0.6