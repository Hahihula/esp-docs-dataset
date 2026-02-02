**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Section Heading:**
20.8 Registers

**Body Text:**
The addresses in this section are relative to the SPI base address provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section **20.7 Register Summary**.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Subsection Title:**
Register 20.1. SPI_CMD_REG (0x0)

**Diagram Description for Subsection:**
- A binary diagram showing the bit positions from leftmost as "31" and rightmost as "0".
- The label next to it reads "SPIUSR".

**Text under Diagram in Subsection:**
SPI_USR An SPI operation will be triggered when this bit is set. The bit will be cleared once the operation is done.

**Subsection Title:**
Register 20.2. SPI_ADDR_REG (0x4)

**Diagram Description for Second Subsection:**
- A binary diagram showing a similar layout as above, but with "31" on both ends.
- There's an indication of reset at position zero and the label next to it reads "Reset".

**Text under Diagram in Second Subsection:**
SPI_ADDR_REG It stores the transmitting address when master is in half-duplex mode or QSPI mode.

If the address length is bigger than 32 bits, this register stores the higher 32 bits of address value. SPI_SLV_WR_STATUS_REG stores the rest lower part of address value. If the address length is smaller than 33 bits, this register stores all the address value. The register is in valid only when SPI_USR_ADDR bit is set to 1.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version:**
ESP32 TRM (Version 5.6)