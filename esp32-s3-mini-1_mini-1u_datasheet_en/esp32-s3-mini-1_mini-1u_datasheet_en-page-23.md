**Title: Peripherals**

---

### Pin Assignment

For TWAI, the pins used can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see [ESP32-S3 Series Datasheet](#) > Section IO Pins and ESP32-S3 Technical Reference Manual > Chapter 10 MUX and GPIO Matrix.

---

### **5.2.1.7 USB 2.0 OTG Full-Speed Interface**

ESP32-S3 features a full-speed USB OTG interface along with an integrated transceiver. The USB OTG interface complies with the USB 2.0 specification.

#### General Features
- FS and LS data rates
- HNP and SRP as A-device or B-device
- Dynamic FIFO (DFIFO) sizing
- Multiple modes of memory access

  - Scatter/Gather DMA mode
  - Buffer DMA mode
  - Slave mode

- Can choose integrated transceiver or external transceiver
- Utilizing integrated transceiver with USB Serial/JTAG by time-division multiplexing when only integrated transceiver is used
- Support USB OTG using one of the transceivers while USB Serial/JTAG using the other one when both integrated transceiver or external transceiver are used

#### Device Mode Features
- Endpoint number 0 always present (bi-directional, consisting of EPO IN and EPO OUT)
- Six additional endpoints (endpoint numbers 1 to 6), configurable as IN or OUT
- Maximum of five IN endpoints concurrently active at any time (including EPO IN)
- All OUT endpoints share a single RX FIFO
- Each IN endpoint has a dedicated TX FIFO

#### Host Mode Features
- Eight channels (pipes)

  - A control pipe consists of two channels (IN and OUT), as IN and OUT transactions must be handled separately. Only Control transfer type is supported.
  
  - Each of the other seven channels is dynamically configurable to be IN or OUT, and supports Bulk, Isochronous, and Interrupt transfer types.

---

**Footer:**
Espressif Systems
23 Submit Documentation Feedback ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6