**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Section Header:**
GoBack

**Subsection with Code and Description:**
- **Code:** `I2S_LC_HUNG_CONF_REG`
  - **Description:** then this interrupt will be triggered.
  
- **Code:** `I2S_RX_HUNG_INT`
  - **Description:** triggered when receiving data is timed out. For example, if I2Sn module is configured as RX slave mode, but the master does not send data for time specified in
    - **Code:** `I2S_LC_HUNG_CONF_REG`, then this interrupt will be triggered.
  
- **Code:** `I2S_TX_DONE_INT`
  - **Description:** triggered when transmitting data is completed.

- **Code:** `I2S_RXDone_INT`
  - **Description:** triggered when receiving data is completed.

**Subsection Title:**
28.13 Register Summary

**Body Text:**
The addresses in this section are relative to [I2Sn] base address provided in Table 4.3-3 in Chapter 4 System and Memory.
The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table with Columns (Name, Description, I2S0 Address, I2S1 Address, Access):**

| Name                           | Description                                                                                   | I2S0 Address | I2S1 Address | Access |
|--------------------------------|------------------------------------------------------------------------------------------------|--------------|--------------|--------|
| Interrupt registers            |                                                                                               |              |              |        |
| `I2S_INT_RAW_REG`             | Interrupt raw register                                                                       | 0x000C       | 0x000C      | RO/WTC/SS |
| `I2S_INT_ST_REG`              | Interrupt status register                                                                    | 0x0010       | 0x0010      | RO     |
| `I2S_INT_ENA_REG`             | Interrupt enable register                                                                    | 0x0014       | 0x0014      | R/W    |
| `I2S_INT_CLR_REG`             | Interrupt clear register                                                                     | 0x0018       | 0x0018      | WT     |
| RX/TX control and configuration registers |                                                                                               |              |              |        |
| `I2S_RX_CONF_REG`            | RX configuration register                                                                      | 0x0020       | varies       | R/W    |
| `I2S_RX_CONF1_REG`           | RX configuration register 1                                                                   | 0x0028       | 0x0028      | R/W    |
| `I2S_RX_CLKM_CONF_REG`        | RX clock configuration register                                                                | 0x0030       | 0x0030      | R/W    |
| `I2S_TX_PCM2PDM_CONF_REG`     | TX PCM-to-PDM configuration register                                                          | 0x0040       | —            | R/W    |
| `I2S_TX_PCM2PDM_CONF1_REG`   | TX PCM-to-PDM configuration register 1                                                        | 0x0044       | —            | R/W    |
| `I2S_RX_TDM_CTRL_REG`         | TX TDM mode control register                                                                  | 0x0050       | 0x0050      | R/W    |
| `I2S_RXEOF_NUM_REG`           | RX data number control register                                                               | 0x0064       | 0x0064      | R/W    |
| `I2S_TX_CONF_REG`             | TX configuration register                                                                      | 0x0024       | varies       | R/W    |
| `I2S_TX_CONF1_REG`            | TX configuration register 1                                                                   | 0x002C       | —            | RO/C   |
| `I2S_TX_CLKM_CONF_REG`        | TX clock configuration register                                                                | 0x0034       | 0x0034      | R/W    |
| `I2S_TX_TDM_CTRL_REG`         | TX TDM mode control register                                                                  | 0x0054       | 0x0054      | R/W    |
| RX clock and timing registers   |                                                                                               |              |              |        |
| `I2S_RX_CLKM_DIV_CONF_REG`    | RX unit clock divider configuration register                                                  | 0x0038       | 0x0038      | R/W    |
| `I2S_RX_TIMING_REG`           | RX timing control register                                                                    | 0x0058       | 0x0058      | R/W    |
| TX clock and timing registers   |                                                                                               |              |              |        |
| `I2S_TX_CLKM_DIV_CONF_REG`    | TX unit clock divider configuration register                                                  | 0x003C       | 0x003C      | R/W    |
| `I2S_TX_TIMING_REG`           | TX timing control register                                                                    | 0x005C       | 0x005C      | R/W    |
| Control and configuration registers |                                                                                               |              |              |        |
| `I2S_LC_HUNG_CONF_REG`        | Timeout configuration register                                                                | 0x0060       | 0x0060      | R/W    |
| `I2S_CONF_SIGLE_DATA_REG`     | Single data register                                                                         | 0x0068       | 0x0068      | R/W    |

**Footer:**
Espressif Systems
1059 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback