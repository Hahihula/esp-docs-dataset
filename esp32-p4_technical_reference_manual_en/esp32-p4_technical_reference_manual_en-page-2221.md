

```markdown
| | | | |
|:----------|:--------|:----|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | | 0 | ADDR_VALUE[31:16] is sent first, and then ADDR_VALUE[15:31—ADDR_BITLEN]. |
| 24~31 | [31:0] | 1 | ADDR_VALUE[31:8] is sent first, and then ADDR_VALUE[ADDR_BITLEN—24:0]. |
| | | 0 | ADDR_VALUE[31:8] is sent first, and then ADDR_VALUE[7:31—ADDR_BITLEN]. |

¹ SPI_USR_ADDR_BITLEN: this field is used to configure the bit length of the address.
² SPI_USR_ADDR_VALUE: address value is written into this field. For which part of this field is used, see the table above.
³ SPI_WR_BIT_ORDER: 0: LSB first; 1: MSB first.

## 43.5.9.3 Full-Duplex Communication (1-bit Mode Only)

### Introduction

GP-SPI supports SPI full-duplex communication. In this mode, SPI master provides CLK and CS signals, exchanging data with SPI slave in 1-bit mode via MOSI (SPI2D/SPI3_D, sending) and MISO (SPI2Q/SPI3_Q, receiving) at the same time. To enable this communication mode, set the bit SPI_DOUTDIN in register SPI_USER_REG. Figure 43.5-6 illustrates the connection of GP-SPI2 with its slave in full-duplex communication.

**Figure 43.5-6. Full-Duplex Communication Between GP-SPI2 Master and a Slave**

In full-duplex communication, the behavior of states CMD, ADDR, DUMMY, DOUT and DIN are configurable. Usually, the states CMD, ADDR and DUMMY are not used in this communication. The bit length of transferred data is configured in SPI_MS_DATA_BITLEN. The actual bit length used in communication equals to (SPI_MS_DATA_BITLEN + 1).

### Configuration (Take GP-SPI2 as an example)

To start a data transfer, follow the steps below:

*   Configure the IO path via IO MUX or GPIO matrix between GP-SPI2 and an external SPI device.
*   Configure AHB clock (AHB_CLK, see Chapter 10 Reset and Clock) and module clock (clk_spi_mst) for the GP-SPI2 module.
*   Set SPI_DOUTDIN and clear SPI_SLAVE_MODE, to enable master full-duplex communication.
*   Configure GP-SPI2 registers listed in Table 43.5-10.
*   Configure SPI CS setup time and hold time according to Section 43.6.
```