

```markdown
Figure 29.5-4. PDM Standard Timing Diagram


## 29.6 I2S TX/RX Clock

I2S_TX/RX_CLK is the master clock of I2S TX/RX unit, divided from:

*   40 MHz XTAL_CLK
*   160 MHz PLL_F160M_CLK
*   240 MHz PLL_D2_CLK
*   or external input clock: I2S_MCLK_in

The serial clock (BCK) of the I2S TX/RX unit is divided from I2S_TX/RX_CLK, as shown in Figure 29.6-1.
I2S_TX/RX_CLK_SEL is used to select clock source for TX/RX unit, and I2S_TX/RX_CLK_ACTIVE to enable or disable the clock source.

Figure 29.6-1. I2S Clock
```