**Title: Chapter 20 SPI Controller (SPI)**

**Subtitle: Register 20.8. SPI_USER_REG (0x1C)**

---

Continued from the previous page...

- **SPI_CS_SETUP**
  - Setting this bit enables a delay between CS active edge and the first clock edge, in multiples of one SPI clock cycle.
  - In full-duplex mode and QSPI mode, setting this bit results in (SPI_SETUP_TIME + 1.5) SPI clock cycles delay.

- **SPI_CS_HOLD**
  - Setting this bit enables a delay between the end of a transmission and CS being inactive, as specified in SPI_HOLD_TIME.
  - Access: Read/Write

- **SPI_DOUTDIN**
  - Set the bit to enable full-duplex communication. (Read/Write)

---

**Subtitle: Register 20.9. SPI_USER1_REG (0x20)**

- **SPI_USR_ADDR_BITLEN**
  - It indicates the bit length of the transmitted address minus one in half-duplex mode and QSPI mode, in multiples of one bit.
  - Access: Read/Write
  - Valid when SPI_USR_ADDR is set to 1.

- **SPI_USR_DUMMY_CYCLEEN**
  - It indicates the number of SPI clock cycles for the dummy phase minus one in SPI half-duplex mode and QSPI mode. 
  - Settable value ranges from 0 to 7.
  - Access: Read/Write
  - Only valid when SPI_USR_DUMMY is set to 1.

---

**Footer Information**
- Page number: 372
- Company name: Espressif Systems
- Document version and type: ESP32 TRM (Version 5.6)
- Link text for feedback submission: Submit Documentation Feedback