

```markdown
Register 35.7. LEDC_TIMERx_CNT_CAP_REG (x: 0-3) (0x01C0+0x4*n)

LEDC_TIMERx_CNT_CAP Represents the captured LEDC timer n counter value. (RO)


Register 35.8. LEDC_CONF_REG (0x01F0)
```

```markdown
LEDC_SCLK_SEL Configures the clock source for the four timers.
0: PLL_F96M_CLK
1: RC_FAST_CLK
2: XTAL_CLK
3: Invalid. No effect
(R/W)

LEDC_GAMMA_RAM_CLK_EN_Ch n Configures when to enable register clock.
0: Support clock only when application reads or writes gamma RAM.
1: Force clock on for gamma RAM.
(R/W)

LEDC_CLK_EN Configures when to enable register clock.
0: Support clock only when application writes registers.
1: Force clock on for registers.
(R/W)
```