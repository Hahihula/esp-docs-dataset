**Title: Chapter 28 I2S Controller (I2S) Register**

**Subtitle: 28.17. I2S_RX_TIMING_REG (0x0058)**

---

### Table:
| Offset | Name                          |
|--------|-------------------------------|
| 31     | [reserved]                   |
| 30-29 | I2S_RX_BCK_IN_DM            |
| 28-27 | I2S_RX_WS_IN_DM             |
| 26-25 | (reserved)                  |
| 24-23 | I2S_RX_OUT_DM               |
| 22     | [reserved]                  |
| 21     | I2S_RX_SD_IN_DM             |
| 20     | (reserved)                  |
| 19     | I2S_RX_SD2_IN_DM            |
| 18-17 | (reserved)                  |
| 16     | [reserved]                  |
| 15     | I2S_RX_WS_OUT_DM           |
| 14     | (reserved)                  |
| 13     | I2S_RX_BCK_IN_DM           |
| 12-11 | (reserved)                  |
| 10-9  | [reserved]                  |
| 8      | Reset                        |

---

### Descriptions:

**I2S_RX_SD_IN_DM**
The delay mode of I2S RX SD input signal. 
- 0: bypass.
- 1: delay by rising edge.

**I2S_RX_SD1_IN_DM (for I2SO only)**
The delay mode of I2S RX SD1 input signal.
- 0: bypass.
- 1: delay by falling edge, not used in R/W

**I2S_RX_SD2_IN_DM (for I2SO only)**
The delay mode of I2S RX SD2 input signal. 
- 0: bypass
- 1: delay by rising edge.

**I2S_RX_SD3_IN_DM (for I2SO only)**
The delay mode of I2S RX SD3 input signal.
- 0: bypass, not used in R/W

**I2S_RX_WS_OUT_DM**
The delay mode of I2S RX WS output signal. 
- 0: bypass
- 1: delay by rising edge.

**I2S_RX_BCK_OUT_DM**
The delay mode of I2S RX BCK output signal.
- 0: bypass, not used in R/W

**I2S_RX_WS_IN_DM**
The delay mode of I2S RX WS input signal. 
- 0: bypass
- 1: delay by rising edge.

**I2S_RX_BCK_IN_DM**
The delay mode of I2S RX BCK input signal.
- 0: bypass, not used in R/W

---

**Footer Information:**

Espressif Systems  
Page Number: 1074  
Document Title: ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)