**Title: Chapter 22 I2S Controller (I2S)**

---

### Register 22.28. I2S_CONFIG_REG (0x00a0)

| Bit | Description |
|-----|-------------|
| **31-0** | Reserved |

#### I2S_TX_STOP_EN
Set this bit and the transmitter will stop transmitting BCK signal and WS signal when tx FIFO is empty.

#### I2S_RX_PCM_BYPASS
Set this bit to bypass the Compress/Decompress module for the received data. (R/W)

#### I2S_RX_PCM_CONF
Compress/Decompress module configuration bit.
- **0:** Decompress received data;
- **1:** Compress received data.

#### I2S_TX_PCM_BYPASS
Set this bit to bypass the Compress/Decompress module for the transmitted data. (R/W)

#### I2S_TX_PCM_CONF
Compress/Decompress module configuration bit.
- **0:** Decompress transmitted data;
- **1:** Compress transmitted data.

---

### Register 22.29. I2S_PD_CONFIG_REG (0x00a4)

| Bit | Description |
|-----|-------------|
| **31-0** | Reserved |

#### I2S_FIFOFORCE_PU
Force FIFO power-up.
- **(R/W)**

#### I2S_FIFOFORCE_PD
Force FIFO power-down. 
- **(R/W)**

---

*Espressif Systems*
*Submit Documentation Feedback*

ESP32 TRM (Version 5.6)