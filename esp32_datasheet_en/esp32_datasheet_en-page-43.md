**4 Functional Description**

---

### Pin Assignment

The pins for SDIO/SPI Slave Controller are multiplexed with GPIO2, GPIO4, GPIO6 ~ GPIO15 via IO MUX.

For more information about the pin assignment, see Section 4.10 Peripheral Pin Configurations and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

---

#### **4.8.12 TWAI® Controller**

The Two-wire Automotive Interface (TWAI®) is a multi-master, multi-cast communication protocol designed for automotive applications. The TWAI controller facilitates the communication based on this protocol.

##### Feature List

- Compatible with ISO 11898-1 protocol (CAN Specification 2.0)
- Standard frame format (11-bit ID) and extended frame format (29-bit ID)
- Bit rates:
  - From 25 Kbit/s to 1 Mbit/s in chip revision v0.0/v1.0/v1.1
  - From 12.5 Kbit/s to 1 Mbit/s in chip revision v3.0/v3.1
- Multiple modes of operation: Normal, Listen Only, and Self-Test
- 64-byte receive FIFO
- Special transmissions: single-shot transmissions and self reception
- Acceptance filter (single and dual filter modes)
- Error detection and handling: error counters, configurable error interrupt threshold, error code capture, arbitration lost capture

For details, see ESP32 Technical Reference Manual > Chapter Two-wire Automotive Interface (TWAI).

---

### Pin Assignment

The pins for the Two-wire Automotive Interface can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section 4.10 Peripheral Pin Configurations and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

---

#### **4.8.13 Ethernet MAC Interface**

An IEEE-802.3-2008-compliant Media Access Controller (MAC) is provided for Ethernet LAN communications. ESP32 requires an external physical interface device (PHY) to connect to the physical LAN bus (twisted-pair, fiber, etc.). The PHY is connected to ESP32 through 17 signals of MII or nine signals of RMII.

##### Feature List

- 10 Mbps and 100 Mbps rates
- Dedicated DMA controller allowing high-speed transfer between the dedicated SRAM and Ethernet MAC
- Tagged MAC frame (VLAN support)

---

Espressif Systems  
43  
ESP32 Series Datasheet v5.2  

[Submit Documentation Feedback](#)