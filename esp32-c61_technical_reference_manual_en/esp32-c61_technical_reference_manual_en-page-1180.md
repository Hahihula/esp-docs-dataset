

```markdown
Chapter 31 LED PWM Controller (LEDC)
GoBack

Register 31.11. LEDC_CONF_REG (0x0170)

LEDC_GAMMA_RAM_CLK_EN_Ch_n (n: 0-5) Configures whether to open LEDC channel n gamma RAM clock gate.
O: Open the clock gate only when an application writes or reads LEDC channel n gamma RAM
1: Force open the clock gate for LEDC channel n gamma RAM
(R/W)

LEDC_CLK_EN Configures whether to open the register clock gate.
O: Open the clock gate only when an application writes registers
1: Force open the clock gate for register
(R/W)

Register 31.12. LEDC_Ch_n_DUTY_R_REG (n: 0-5) (0x0010+0x14*n)

LEDC_DUTY_Ch_n_R Represents the current duty cycle of output signal on channel n. (RO)

Register 31.13. LEDC_TIMER_x_VALUE_REG (x: 0-3) (0x00A4+0x8*x)

LEDC_TIMER_x_CNT Represents the current counter value of timer x. (RO)
```