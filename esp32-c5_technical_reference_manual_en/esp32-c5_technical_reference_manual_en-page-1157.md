

```markdown
## 33.11 Register

**Notice:**
ESP32-C5 does not currently support the functions associated with the fields marked with HRO access in this section.

The addresses in this section are relative to GP-SPI2 base address provided in Table 6.3-2 in Chapter 6 *System and Memory*.

For how to program reserved fields, please refer to Section *Programming Reserved Register Field*.

### Register 33.1. SPI_CMD_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 31:25 | (reserved) |
| 24 | `SPI_CONF_BITLEN` Configures the SPI_CLK cycles of SPI CONF state.<br>Measurement unit: SPI_CLK clock cycle.<br>Can be configured in CONF state.<br>(R/W) |
| 23 | `SPI_UPDATE` Configures whether or not to synchronize SPI registers from APB clock domain into SPI module clock domain.<br>O: Not synchronize<br>1: Synchronize<br>This bit is only used in SPI master transfer.<br>(WT) |
| 22 | `SPI_USR` Configures whether or not to enable user-defined command.<br>O: Not enable<br>1: Enable<br>An SPI operation will be triggered when the bit is set. This bit will be cleared once the operation is done. Can not be changed by CONF_buf.<br>(R/W/SC) |
| 21 | (reserved) |
| 20 | `SPI_USR_UPDATE` Configures whether or not to enable user-defined command update.<br>O: Not enable<br>1: Enable<br>This bit will trigger an SPI operation when set. It is cleared after the operation completes and cannot be changed by CONF_buf.<br>(R/W/SC) |
| 19 | (reserved) |
| 18 | `SPI_CONF_BITLEN` Configures the SPI_CLK cycles of SPI CONF state.<br>Measurement unit: SPI_CLK clock cycle.<br>Can be configured in CONF state.<br>(R/W) |
| 17 | Reset |

```
*Note:* The diagram appears to represent a bit field layout for register `SPI_CMD_REG (0x0000)` with labeled bits and their descriptions. Some fields are marked as reserved or have specific behaviors like write-through (WT), write-set-clear (SC), etc., consistent with typical SPI controller register documentation.
```