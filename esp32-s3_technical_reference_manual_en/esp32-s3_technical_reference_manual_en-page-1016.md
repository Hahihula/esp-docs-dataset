**Title: Chapter 27 I2C Controller (I2C)**

**Subtitle: Register Summary**

The addresses in this section are relative to **I2C Controller** base address provided in Table A.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| Timing registers | Configures the low level width of SCL | `0x0000` | R/W |
| I2C_SCL_LOW_PERIOD_REG | Configures the hold time after a negative SCL edge | `0x0030` | R/W |
| I2C_SDA_HOLD_REG | Configures the sample time after a positive SCL edge | `0x0044` | R/W |
| I2C_SCL_HIGH_PERIOD_REG | Configures the high level width of SCL | `0x0058` | R/W |
| I2C_SCL_START_HOLD_REG | Configures the delay between the SDA and SCL negative edge for a START condition | `0x0064` | R/W |
| I2C_SCL_RSTART_SETUP_REG | Configures the delay between the positive edge of SCL and the negative edge of SDA | `0x0078` | R/W |
| I2C_SCL_STOP_HOLD_REG | Configures the delay after the SCL clock edge for a STOP condition | `0x0094` | R/W |
| I2C_SCL_STOP_SETUP_REG | Configures the delay between the SDA and SCL positive edge for a STOP condition | `0x00A8` | R/W |
| I2C_SCL_ST_TIME_OUT_REG | SCL status timeout register | - | RO |

**Configuration registers**

- **I2C_CTR_REG**: Transmission configuration register (`0x0004`) varies
- **I2C_TO_REG**: Timeout control register (`0x0018`) R/W
- **I2C_SLAVE_ADDR_REG**: Slave address configuration register (`0x0030`) R/W
- **I2C_FIFO_CONF_REG**: FIFO configuration register (`0x0044`) RO
- **I2C_FILTER_CFG_REG**: SCL and SDA filter configuration register (`0x0058`) varies
- **I2C_CLK_CONF_REG**: I2C clock configuration register (`0x0064`) R/W
- **I2C_SCL_SP_CONF_REG**: Power configuration register (`0x0078`) RO

**Status registers**

- **I2C_SR_REG**: Describes I2C work status (`0x0084`) varies
- **I2C_FIFO_ST_REG**: FIFO status register (`0x0098`) R/W
- **I2C_DATA_REG**: Read/write FIFO register (`0x00A4`) RO

**Interrupt registers**

- **I2C_INT_RAW_REG**: Raw interrupt status (`0x00B8`) varies
- **I2C_INT_CLR_REG**: Interrupt clear bits (`0x00C4`) WT
- **I2C_INT_ENA_REG**: Interrupt enable bits (`0x00D8`) R/W

**Command registers**

- **I2C_COMDO_REG**: I2C command register 0 (`0x0100`) varies

---

*Espressif Systems*
*Page: 1016*

*ESP32-S3 TRM (Version 1.7)*
*Submit Documentation Feedback*