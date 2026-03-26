

```markdown
Chapter 55 LED PWM Controller (LEDC)

Register 55.11. LEDC_CONF_REG (0x0170)
| Bit | Description |
|-----|-------------|
| 31:30 | (reserved) |
| 9   | LEDC_GAMMA_RAM_CLK_EN_CHn (n: 0-7) Configures whether to open LEDC channel n gamma RAM clock gate. O: Open the clock gate only when an application writes or reads LEDC channel n gamma RAM<br>1: Force open the clock gate for LEDC channel n gamma RAM (R/W) |
| 8   | LEDC_CLK_EN Configures whether to open the register clock gate.<br>O: Open the clock gate only when an application writes registers<br>1: Force open the clock gate for register (R/W) |

Register 55.12. LEDC_CHn_DUTY_R_REG (n: 0-7) (0x0010+0x14*n)
| Bit | Description |
|-----|-------------|
| 31:26 | (reserved) |
| 25   | LEDC_DUTY_CHn_R Represents the current duty cycle of output signal on channel n. (RO) |

Register 55.13. LEDC_TIMERx_VALUE_REG (x: 0-3) (0x0A4+0x8*x)
| Bit | Description |
|-----|-------------|
| 31:20 | (reserved) |
| 19   | LEDC_TIMERx_CNT Represents the current counter value of timer x. (RO) |
```