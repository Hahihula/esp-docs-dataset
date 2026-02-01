**4 Functional Description**

- **Scatter/Gather DMA mode**
- **Buffer DMA mode**
- **Slave Mode**
- Integrated UMTI High-Speed transceiver

**Device Mode Features**
- Endpoint 0 always present, bi-directional, consisting of EPO IN and EPO OUT
- 15 additional endpoints 1–15, configurable as IN or OUT
- Maximum of eight IN endpoints concurrently active at any time, including EPO IN
- All OUT endpoints share a single RX FIFO
- Each IN endpoint has a dedicated TX FIFO

**Host Mode Features**
- **16 host channels**
- RX FIFO: shared by all periodic and non-periodic transactions
- Two TX FIFO:
  - One shared by all non-periodic transactions
  - One shared by all periodic transactions
- All of the above FIFOs share a 4 KB RAM.
- The size of each FIFO is configurable, with a maximum of 4 KB.

**Pin Assignment**
The pins connected to USB2 OTG PHY DM (USB_D-) and USB2 OTG PHY DP (USB_D+) signals of USB 2.0 High-Speed OTG are dedicated pin49 and pin50. Other signals can be routed to any GPIOs via the GPIO matrix.

**4.2.2.10 USB 2.0 Full-Speed OTG**

The ESP32-P4 features a USB 2.0 Full-Speed On-The-Go peripheral (henceforth referred to as OTG_FS) along with integrated transceivers. This OTG_FS conforms to USB 2.0 specification, OTG Revision 1.3, and OTG Revision 2.0 specifications. OTG_FS can operate as either a USB Host or Device and supports 12 Mbit/s full-speed (FS) and 1.5 Mbit/s low-speed (LS) data rates of the USB 2.0 specification. The Host Negotiation Protocol (HNP) and the Session Request Protocol (SRP) are also supported.

**Feature List**

**General Features**
- USB 2.0 specification, OTG Revision 1.3 and OTG Revision 2.0 specifications
- USB 2.0 full-speed and low-speed data rates
- HNP and SRP as A-device or B-device

Espressif Systems  
68 ESP32-P4 Series Datasheet v0.6  

[Submit Documentation Feedback](#)