**Chapter Title:**
Chapter 23 Pulse Count Controller (PCNT)

**Section Header:**
Register 23.9. PCNT_CTRL_REG (0x00b0)

**Table Description for Register 23.9, PCNT_CTRL_REG:**

| Bit | Name                          |
|-----|-------------------------------|
| 17  | PONT_CLK_EN                  |
|     | Configures register clock gating. |
|     | - O: Support clock only when the application writes registers. |
|     | - 1: Always force the clock on for registers. (R/W) |
| 0   | PCNT_CNT_PAUSE_Un            |
|     | Set this bit to freeze unit n's counter. (R/W) |
|     | PCNT_PLUS_CNT_RST_Un         |
|     | Set this bit to clear unit n's counter. (R/W) |

**Section Header:**
Register 23.10, PCNT_UN_STATUS_REG (n: 0-7) (0x90+0xC*n)

**Table Description for Register 23.10, PCNT_UN_STATUS_REG:**

| Bit | Name                          |
|-----|-------------------------------|
|     | The last interrupt happened on counter for unit n reaching O. (RO) |
|     | - PCNT_THR_ZERO_LAT_Un       |
|     | - PCNT_THR_H_LIM LAT_Un      |
|     | - PCNT_THR_L_LIM LAT_Un      |
|     | - PCNT_THRThRESO LAT_Un      |
|     | - PCNT_THRTHRES1 LAT_Un      |
| 0   | PCNT_THR_ZERO_MODE_Un        |
|     | This register stores the current status of the counter. O: counting value is +0 (the counter values are represented by signed binary numbers); 1: counting value is negative; -2: counting value is positive. (RO) |

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Type:**
ESP32 TRM (Version 5.6)

**Navigation Link:**
GoBack