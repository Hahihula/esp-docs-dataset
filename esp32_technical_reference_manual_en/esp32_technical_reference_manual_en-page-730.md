**Chapter Title:**
- Chapter 30 Remote Control Peripheral (RMT)

**Subsections and Descriptions:**
1. **RMT_CHn_TX_END_INT:** Triggered when the transmitter has finished transmitting the signal.
2. **RMT_CHn_RX_END_INT:** Triggered when the receiver has finished receiving a signal.

**Section Title: 30.3 Register Summary**

**Body Text:**
- The addresses in this section are relative to the RMT base address provided in Table 3.3-6 in Chapter 3 System and Memory.
- The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Content (with headers):**
- **Name:** Configuration registers, Interrupt registers, Carrier wave duty cycle registers, Tx event configuration registers
- **Description:**
  - Channel O config register 0
  - RMT CHOCONF0 REG
  - ...
  - Raw interrupt status
  - Masked interrupt status
  - Interrupt enable bits
  - Channel X duty cycle configuration register (where X ranges from 1 to 7)
  - Tx event configuration register

**Table Entries:**
- **Address:** Each entry has an address specified in hexadecimal format.
- **Access:** Indicates whether the access is Read/Write or Write Only.

**Footer Information:**
- Espresso Systems
- Page number and document version information (ESP32 TRM [Version 5.6])