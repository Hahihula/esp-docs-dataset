**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Table Header:**
Table 30.5-10. Sending Sequence of Address Value

| ADDR_BITLEN^1 | ADDR_VALUE^2 | BIT_ORDER^3 | Sending Sequence of Address Value |
|----------------|--------------|-------------|----------------------------------|
| O - 7          | [31:24]      | 1           | COMMAND_VALUE[ADDR_BITLEN + 24:24] is sent first. |
|                |              |             | ADDR_VALUE[31:31 - ADDR_BITLEN] is sent first. |
| 8 - 15         | [31:16]      | 1           | ADDR_VALUE[31:24] is sent first, and then ADDR_VALUE[ADDR_BITLEN + 8:16] is sent. |
|                |              |             | ADDR_VALUE[23:31 - ADDR_BITLEN] is sent. |
| 16 - 23        | [31:8]       | 1           | ADDR_VALUE[31:16] is sent first, and then ADDR_VALUE[ADDR_BITLEN - 8:8] is sent. |
|                |              |             | ADDR_VALUE[31:16] is sent first, and then ADDR_VALUE[15:31 - ADDR_BITLEN] is sent. |
| 24 - 31        | [31:0]       | 1           | ADDR_VALUE[31:8] is sent first, and then ADDR_VALUE[ADDR_BITLEN - 24:0] is sent. |
|                |              |             | ADDR_VALUE[31:8] is sent first, and then ADDR_VALUE[7:31 - ADDR_BITLEN] is sent. |

**Footnotes in Table:**
^1 SPI_USR_ADDR_BITLEN: this field is used to configure the bit length of the address.
^2 SPI_USR_ADDR_VALUE: address value is written into this field. For which part of this field is used, see the table above.

^3 SPI_WR BIT_ORDER: 0: LSB first; 1: MSB first.

**Section Title and Subtitle:**
30.5.8.3 Full-Duplex Communication (1-bit Mode Only)

**Subsection Header - Introduction:**

GP-SPI supports full-duplex communication. In this mode, SPI master provides CLK and CS signals, exchanging data with SPI slave in 1-bit mode via MOSI (FSPID/SPI3_D, sending) and MISO (FSPIQ/SPI3_Q, receiving) at the same time. To enable this communication mode, set the bit SPI_DOUTDIN in register SPI_USER_REG. Figure 30.5-6 illustrates the connection of GP-SPI2 with its slave in full-duplex communication.

**Figure Description:**
Figure 30.5-6 shows Full-Duplex Communication Between GP-SPI2 Master and a Slave, depicting connections between GP-SPI2 (Master), FSPID, MOSI, MISO, FSPICLK, CLK, CS, FSPIO, and FSPICS.

**Additional Information:**
In full-duplex communication, the behavior of states CMD, ADDR, DUMMY, DOUT, and DIN are configurable. Usually, the states CMD, ADDR, and DUMMY are not used in this communication. The bit length of transferred data is specified by the ADDR_BITLEN field.
  
**Footer Information:**
Espressif Systems
1128 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback