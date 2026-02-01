**Title: Functional Description**

- **RMII Group 2:** Signals are multiplexed with GPIO40–GPIO48 via IO MUX.
- **RMII Group 3:** Provides partial signal routing (excluding transmit signals except for RMII_TXEN) and is multiplexed with GPIO49–GPIO54 via IO MUX.

Each RMII signal can be assigned independently to any of these three groups to form a complete RMII interface. The MI1 interface, MDIO interface, and other peripheral signals can be routed to any GPIO via the GPIO Matrix for additional flexibility.

**Subtitle: 4.2.2.13 Two-Wire Automotive Interface (TWAI)**

ESP32-P4 contains three TWAI controllers. Each controller can individually be connected to a TWAI bus via an external transceiver.

**Feature List**
- Compatibility with ISO 11898-1 protocol (CAN Specification 2.0)
- Standard Frame Format (11-bit ID) and Extended Frame Format (29-bit ID)
- Bit rates from 1 Kbit/s to 1 Mbit/s
- Multiple modes of operation:
  - Normal
  - Listen-only (no influence on bus)
  - Self-test (no acknowledgment required during data transmission)
- 64-byte Receive FIFO

**Special transmissions:**
- Single-shot transmissions (does not automatically re-transmit upon error)
- Self-reception (the TWAI controller transmits and receives messages simultaneously)

**Acceptance Filter:** supports Single and Dual-filter modes
- Error detection and handling:
  - Error counters
  - Configurable error warning limit
  - Error code capture
  - Arbitration lost capture
  - Automatic transceiver standby

**Pin Assignment**
The pins for the two-wire automotive interface can be chosen from any GPIOs via the GPIO Matrix.

---

Espressif Systems  
Submit Documentation Feedback  
ESP32-P4 Series Datasheet v0.6