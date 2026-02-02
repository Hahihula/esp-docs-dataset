**Title: Chapter 28 LED PWM Controller (LEDC)**

---

### Register 28.5, LEDC_HSCHn_DUTY_R_REG (n: 0-7) (0x10+0x14*n)

| Bit | Description |
|-----|-------------|
| 31  | Reserved    |
| 25  |             |
| 24  |             |
| ... |             |
| 0   |             |

**LEDC_DUTY_HSCHn_R**: This register represents the current duty cycle of the output signal for high-speed channel n. (RO)

---

### Register 28.6, LEDC_LSCHn_CONFO_REG (n: 0-7) (0xA0+0x14*n)

| Bit | Description |
|-----|-------------|
| 31  | Reserved    |
| ... |             |
| 5   |             |
| 4   |             |
| 3   |             |
| 2   |             |
| 1   |             |
| 0   |             |

**LEDC_PARA_UP_LSCHn**: This bit is used to update register LE DC_LSCHn_HPOIN T and LE DC_LSCHn_DUTY for low-speed channel n. (R/W)

**LEDC_IDLE_LV_LSCHn**: This bit is used to control the output value, when low-speed channel n is inactive. (R/W)

**LEDC_SIG_OUT_EN_LSCHn**: This is the output enable control bit for low-speed channel n. (R/W)

**LEDC_TIMER_SEL_LSCHn**: There are four low-speed timers; the two bits are used to select one of them for low-speed channel n. (R/W)
- 0: select I timer0;
- 1: select I timer1;
- 2: select I timer2;
- 3: select I timer3.

---

**Footer**: Espressif Systems, ESP32 TRM (Version 5.6)  
[Submit Documentation Feedback](#)