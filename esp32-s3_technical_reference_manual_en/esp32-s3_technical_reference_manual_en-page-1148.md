Title: Chapter 30 SPI Controller (SPI)

Subtitle: GoBack

Section Title: 30.9 Differences Between GP-SPI2 and GP-SPI3

Body Text:
The feature differences between GP-SPI2 and GP-SPI3 are as follows:

- The communication mode for each GP-SPI2 state (CMD, ADDR, DOUT or DIN) can be configured independently. Data can either be in 1/2/4/8-bit master mode or 1/2/4-bit slave mode. Whereas GP-SPI3 supports 1/2/4-bit master mode or 1/2/4-bit slave mode.
- DMA-controlled configurable segmented transfer is only supported in GP-SPI2. Therefore, CONF state is not used in GP-SPI3.
- The I/O lines of GP-SPI2 can be mapped to physical GPIO pins either via GPIO matrix or IO MUX. However, GP-SPI3 lines can be configured only via GPIO matrix.

GP-SPI2 has six CS signals in master mode. GP-SPI3 only has three CS signals in master mode.
Apart from that, the functions of GP-SPI2 and GP-SPI3 are the same. GP-SPI2 can use all the GP-SPI registers, while GP-SPI3 can only use some of the GP-SPI registers, see Table 30.9-1 for details.

Table Title: Table 30.9-1. Invalid Registers and Fields for GP-SPI3

Table:
| Invalid Register | Invalid Field |
|------------------|---------------|
| SPI_USER_REG     | SPI_OPI_MODE  |
|                  | SPI_FWRITE_OCT|
| SPI_CTRL_REG     | SPI_FADDR_OCT |
|                  | SPI_FCMD_OCT  |
|                  | SPI_FREDOCT   |
|                  | SPI_CS3_DIS    |
|                  | SPI_CS4_DIS    |
|                  | SPI_CS5_DIS    |
| SPI_MISC_REG     | SPI_CS6_DIS    |
|                  | SPI_MASTER_CS_POL[5:3]|
|                  | SPI_DIN4_MODE  |
|                  | SPI_DIN5_MODE  |
|                  | SPI_DIN6_MODE  |
|                  | SPI_DIN7_MODE  |
|                  | SPI_DIN4_NUM   |
|                  | SPI_DIN5_NUM   |
|                  | SPI_DIN6_NUM   |
|                  | SPI_DIN7_NUM   |
|                  | SPI_DOUT4_MODE |
|                  | SPI_DOUT5_MODE |
|                  | SPI_DOUT6_MODE |
|                  | SPI_DOUT7_MODE |

Body Text:
GP-SPI3 has the same 1/2/4-bit mode functions and register configuration rules as to GP-SPI2. GP-SPI3 interface can be seen as a 1/2/4-bit mode GP-SPI2 interface, without DMA-controlled configurable segmented transfer.

Footer: Espressif Systems
Page Number: 1148
Document Version Information: ESP32-S3 TRM (Version 1.7)
Link Texts:
- Submit Documentation Feedback

(Note: The text "Table" is part of the table header and not a separate section title.)