

```markdown
Chapter 40 LED PWM Controller (LEDC) GoBack

Register 40.11. LEDC_CONF_REG (0x0170)

LEDC_GAMMA_RAM_CLK_EN_Ch(n: 0-5) Configures whether to open LEDC channel n gamma RAM clock gate.
O: Open the clock gate only when an application writes or reads LEDC channel n gamma RAM
1: Force open the clock gate for LEDC channel n gamma RAM (R/W)

LEDC_CLK_EN Configures whether to open the register clock gate.
O: Open the clock gate only when an application writes registers
1: Force open the clock gate for register (R/W)

Register 40.12. LEDC_Ch(n)_DUTY_R_REG (n: 0-5) (0x0010+0x14*n)

LEDC_DUTY_Ch(n)_R Represents the current duty cycle of output signal on channel n. (RO)

Register 40.13. LEDC_TIMERx_VALUE_REG (x: 0-3) (0x0A4+0x8*x)

LEDC_TIMERx_CNT Represents the current counter value of timer x. (RO)
```