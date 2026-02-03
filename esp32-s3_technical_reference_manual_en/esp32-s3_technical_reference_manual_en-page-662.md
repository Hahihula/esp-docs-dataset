**Title:**
Chapter 12 Timer Group (TIMG)

**Subtitle:**
12.5 Registers

**Body Text:**

The addresses in this section are relative to Timer Group base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Table Description for Register 12.1, TIMG_TxCONFIG_REG (x : 0-1) (0x0000+0x24*x):**

| Address | Binary Value |
|---------|--------------|
| 31      | 0            |
| 30      | 1            |
| 29      | 0            |
| 28      | 0            |
|         |             |
| 13      | 0            |
| 12      | 0            |
| 11      | 0            |
| 10      | 0            |
| 9       | 0            |
| 8        | 0            |
| (reserved) |             |
| TIMG_TX_EN |           |
| TIMG_TX_INCREASE |    |
| TIMG_TX_DIVIDER |   |
| TIMG_TX_ALARMMEN |     |
| TIMG_TX_USE_XTAL |      |

**Description for each bit:**
- TIMG_Tx_USE_XTAL (0): Use APB_CLK as the source clock of timer group; 1: Use XTLAL_CLK as the source clock of timer group. (R/W)
- TIMG_Tx_ALARM_EN When set, the alarm is enabled. This bit is automatically cleared once an alarm occurs. (R/W/SC)
- TIMG_Tx_DIVIDER Timer x clk prescaler value. (R/W)
- TIMG_Tx_AUTORELOAD When set, timer x auto-reload at alarm is enabled. (R/W)
- TIMG_Tx_INCREASE When set, the timer x time-base counter will increment every clock tick. When cleared, the timer x time-base counter will decrement. (R/W)
- TIMG_Tx_EN When set, the timer x time-base counter is enabled. (R/W)

**Table Description for Register 12.2, TIMG_Tx_LO_REG (x : 0-1) (0x0004+0x24*x):**

| Address | Binary Value |
|---------|--------------|
| 31      | 0            |
|         |             |
| 0       | 0            |

**Description for each bit:**
- TIMG_Tx_LO After writing to TIMG_TxUPDATE_REG, the low 32 bits of the time-base counter of timer x can be read here. (RO)

**Footer Information:**

Espressif Systems
662

Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)