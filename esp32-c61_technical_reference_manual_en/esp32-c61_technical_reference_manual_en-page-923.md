

```markdown
## 26.11 Register

**Notice:**
ESP32-C61 does not currently support the functions associated with the fields marked with HRO access in this section.

The addresses in this section are relative to GP-SPI2 base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 26.1. SPI_CMD_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 31:25 | reserved |
| 24 | SPI_CONF_BITLEN |
| 23 | SPI_UPDATE |
| 22 | SPI_USR |
| 18-17 | reserved |
| 16 | Reset |

**SPI_CONF_BITLEN** Configures the SPI_CLK cycles of SPI CONF state.
Measurement unit: SPI_CLK clock cycle.
Can be configured in CONF state.
(R/W)

**SPI_UPDATE** Configures whether or not to synchronize SPI registers from APB clock domain into SPI module clock domain.
O: Not synchronize
1: Synchronize
This bit is only used in SPI master transfer.
(WT)

**SPI_USR** Configures whether or not to enable user-defined command.
O: Not enable
1: Enable
An SPI operation will be triggered when the bit is set. This bit will be cleared once the operation is done. Can not be changed by CONF_buf.
(R/W/SC)
```