

```markdown\nFigure 46.5-4. PDM Standard Timing Diagram\n```
## 46.6 I2S TX/RX Clock

I2Sn_TX/RX_CLK is the master clock of I2Sn TX/RX unit, divided from:

*   40 MHz XTAL_CLK
*   160 MHz PLL_F160M_CLK
*   APLL_CLK with adjustable frequency
*   I2Sn_MCLK_in (external input clock)

The serial clock (BCK) of the I2Sn TX/RX unit is divided from I2Sn_TX/RX_CLK, as shown in Figure 46.6-1.

HP_SYS_CLKRST_I2Sn_SRC_SEL is used to select clock source for TX/RX unit, and HP_SYS_CLKRST_I2Sn_TX/RX_CLK_EN to enable or disable the clock source.

```markdown
Figure 46.6-1. I2Sn Clock Generator
```
```markdown\nEspressif Systems                          2454                ESP32-P4 TRM\nSubmit Documentation Feedback            PRELIMINARY
```