**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Register Information:**
- Register Name: EMACLPI_CSR_REG (0x1030)
- Layout:
  - LPITXA, LPIEN, RLPST, TLPIEN

**Bit Definitions and Descriptions:**

- **LPITXA:** This bit controls the behavior of the MAC when it is entering or coming out of the LPI mode on the transmit side. If the LPITXA and LPIEN bits are set to 1, the MAC enters the LPI mode only after all outstanding frames and pending frames have been transmitted. The MAC comes out of the LPI mode when an application sends any frame. When this bit is 0, the LPIEN bit directly controls behavior of the MAC when it is entering or coming out of the LPI mode.

- **PLS:** This bit indicates the link status of the PHY. When set, the link is considered to be okay (up) and when reset, the line is considered to be down.
  - Access: Read/Write

- **LPIEN:** When this bit instructs the MAC Transmitter to enter into LPI state. When reset, it indicates that the MAC should exit from LPITXA mode after receiving a new packet for transmission.

- **RLPIST:** Indicates when the MAC is in MII interface and receives an LPI pattern.
  - Access: Read/Write

- **TLPIST:** Indicates when the MAC has received data on TLPIEN state, indicating that it should resume normal reception of packets after receiving a new packet for transmission.

- **RLPIEX:** When set indicates that the MAC Receiver is in MII interface and resumes LPI pattern.
  - Access: Read/SS/RC

- **RLPIEN:** Indicates when the MAC has received an LPITXA state, indicating it should resume normal reception after receiving a new packet for transmission.

- **TLPIEX:** When set indicates that the MAC Transmitter is in MII interface and resumes LPI pattern.
  - Access: Read/SS/RC

- **TLPIEN:** Indicates when the MAC has entered an LPITXA state, indicating it should resume normal reception after receiving a new packet for transmission.

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Link:
  - ESP32 TRM (Version 5.6)
  - Submit Documentation Feedback