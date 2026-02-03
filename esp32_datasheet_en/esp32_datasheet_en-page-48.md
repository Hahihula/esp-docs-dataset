**Title: Functional Description**

---

| Interface | Signal | Pin | Function |
|-----------|--------|-----|----------|
| **SD/SDIO/MMC Host Controller** | HS2_CLK | MTMS | Supports SD memory card V3.01 standard |
| | HS2_CMD | MDTO |  |
| | HS2_DATA0 | GPIO2 |  |
| | HS2_DATA1 | GPIO4 |  |
| | HS2_DATA2 | MTDI |  |
| | HS2_DATA3 | MTCK |  |
| | PWM0_OUT0~2 | Any | Three channels of 16-bit timers generate PWM waveforms. Each channel has a pair of output signals, three fault detection signals, three event-capture signals, and three sync signals. |
| **Motor PWM** | PWM1_OUT_INO~2 | Any GPIO Pins |  |
| | PWM0_FLT_INO~2 | Any GPIO Pins |  |
| | PWM0_FLT_INO~2 | Any GPIO Pins |  |
| | PWM0_CAP_INO~2 | Any GPIO Pins |  |
| | PWM1_INO~2 | Any GPIO Pins |  |
| | PWM0_SYNC_INO~2 | Any GPIO Pins |  |
| **SDIO/SPI Slave Controller** | SD_CLK | MTMS | SDIO interface that conforms to the industry standard SDIO 2.0 card specification |
| | SD_CMD | MDTO |  |
| | SD_DATA0 | GPIO2 |  |
| | SD_DATA1 | GPIO4 |  |
| | SD_DATA2 | MTDI |  |
| | SD_DATA3 | MTCK |  |
| **UART** | UORXD_in | Any GPIO Pins | Three UART devices with hardware flow-control and DMA |
| | UOCTS_in | Any GPIO Pins |  |
| | UODSR_in | Any GPIO Pins |  |
| | UOTXD_out | Any GPIO Pins |  |
| | UORTS_out | Any GPIO Pins |  |
| **I2C** | U1RXD_in | Any GPIO Pins | Two I2C devices in slave or master mode |
| | U1CTS_in | Any GPIO Pins |  |
| | U1TXD_out | Any GPIO Pins |  |
| | U1RTS_out | Any GPIO Pins |  |
| **I2CEXT0_SCL_in** | I2CEXT0_SCL_in | Any GPIO Pins | Two I2C devices in slave or master mode |
| | I2CEXT0_SDA_in | Any GPIO Pins |  |
| | I2CEXT1_SCL_in | Any GPIO Pins |  |
| | I2CEXT1_SDA_in | Any GPIO Pins |  |
| **I2CEXT1_SCL_out** | I2CEXT1_SCL_out | Any GPIO Pins | Two I2C devices in slave or master mode |
| | I2CEXT1_SDA_out | Any GPIO Pins |  |

---

*Espressif Systems  
ESP32 Series Datasheet v5.2*

[Submit Documentation Feedback](#)