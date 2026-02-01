Title: Functional Description

- Acceptance filter (single and dual filter modes)
- Error detection and handling:
  - Error counters
  - Configurable error interrupt threshold
  - Error code capture
  - Arbitration lost capture

For details, see ESP32-S3 Technical Reference Manual > Chapter Two-wire Automotive Interface.

Subtitle: Pin Assignment

For details, see Section 2.3.5 Peripheral Pin Assignment.

Title: USB 2.0 OTG Full-Speed Interface (4.217)

ESP32-S3 features a full-speed USB OTG interface along with an integrated transceiver. The USB OTG interface complies with the USB 2.0 specification.

Subtitle: General Features

- FS and LS data rates
- HNP and SRP as A-device or B-device
- Dynamic FIFO (DFIFO) sizing
- Multiple modes of memory access:
  - Scatter/Gather DMA mode
  - Buffer DMA mode
  - Slave mode
- Can choose integrated transceiver or external transceiver
- Utilizing integrated transceiver with USB Serial/JTAG by time-division multiplexing when only integrated transceiver is used
- Support USB OTG using one of the transceivers while USB Serial/JTAG using the other one when both integrated transceiver or external transceiver are used

Subtitle: Device Mode Features

- Endpoint number 0 always present (bi-directional, consisting of EPO IN and EPO OUT)
- Six additional endpoints (endpoint numbers 1 to 6), configurable as IN or OUT
- Maximum of five IN endpoints concurrently active at any time (including EPO IN)
- All OUT endpoints share a single RX FIFO
- Each IN endpoint has a dedicated TX FIFO

Footer: Espressif Systems, Submit Documentation Feedback ESP32-S3 Series Datasheet v2.1