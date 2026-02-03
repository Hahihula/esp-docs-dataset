**Title: Chapter 30 SPI Controller (SPI)**

**Subtitle: Register 30.8. SPI_MISD_REG (For SPI2 Only) (0x0020)**

**Table Description:**  
The table lists various registers related to the SPI controller, with their bit positions and descriptions.

- **SPI_QUAD_DIN_PIN_SWAP**
- **SPI_CS KEEP ACTIVE EDGE**
- **SPI_CS POL**
- **SPI_DOs EDGE**
- **SPI_DOs POL**
- **SPI_MST_DIN**
- **SPI_MST_DOUT**
- **SPI_MST_DPOL**
- **SPI_MST_DQS**

**Bit Positions:**
- 31 to 0 (with some bits reserved)

**Reset Values:**  
The reset values for each bit are provided in the table.

**Descriptions of SPI Control Registers and their Functions:**

- **SPI_CS0_DIS**: SPI CS0 pin enable bit. 1: disable CSO.
- **SPI_CS1_DIS**: SPI CS1 pin enable bit. 1: disable CS1 (R/W).
- **SPI_CS2_DIS**: SPI CS2 pin enable bit. 1: disable CS2
- **SPI_CS3_DIS**: SPI CS3 pin enable bit. 1: disable CS3.
- **SPI_CS4_DIS**: SPI CS4 pin enable bit. 1: disable CS4 (R/W).
- **SPI_CS5_DIS**: SPI CS5 pin enable bit. 1: disable CS5
- **SPI_CLK_DIS**: Disable SPI_CLK output, or Enable SPI_CLK output in CONF state.
- **SPI_MASTER_CS_POL**: Configures the polarity of SPI CS line in master mode; can be configured to high active (1) and low active (0).
- **SPI_CLK_DATA_DTR_EN**: SPI master DDR mode is applied to SPI clock, data, and SPI_DQS
- **SPI_DATA_DTR_EN**: SPI clock and data states are in DDR mode.
- **SPI_ADDR_DTR_EN**: SPI clock state of SPI_SEND_ADDR line; can be configured as SDR or DDR (R/W).
- **SPI_CMD_DTR_EN**: SPI clock and data states for SPI_SEND_CMD lines
- **SPI_SLAVE_CS_POL**: Configure SPI slave input CS polarity

**Footer:**
"Continued on the next page..."
"ESP32-S3 TRM (Version 1.7)"
"Submit Documentation Feedback"

**Page Number:** 
1159