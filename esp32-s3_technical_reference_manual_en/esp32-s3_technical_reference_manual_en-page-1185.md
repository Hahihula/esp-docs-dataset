**Chapter Title:**
Chapter 31

**Section Titles and Content:**

- **Two-wire Automotive Interface (TWAI®) Overview**
  - The Two-wire Automotive Interface (TWAI®) is a multi-master, multi-cast communication protocol with error detection and signaling and inbuilt message priorities and arbitration. It's suited for automotive and industrial applications.

- **Features of ESP32-S3 TWAI controller:**
  - Compatible with ISO 11898-1 protocol (CAN Specification 2.0)
  - Supports Standard Frame Format (11-bit ID) and Extended Frame Format (29-bit ID)
  - Bit rates from 1 Kbit/s to 1 Mbit/s
  - Multiple modes of operation:
    - Normal
    - Listen-only (no influence on bus)
    - Self-test (no acknowledgment required during data transmission)
  - 64-byte Receive FIFO
  - Special transmissions:
    - Single-shot transmissions (does not automatically re-transmit upon error)
    - Self Reception (the TWAI controller transmits and receives messages simultaneously)
  - Acceptance Filter: supports single and dual filter modes.
  - Error detection and handling:
    - Error Counters
    - Configurable Error Warning Limit
    - Error Code Capture
    - Arbitration Lost Capture

**Footer Information:**
- Page number: 1185
- Document version: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems