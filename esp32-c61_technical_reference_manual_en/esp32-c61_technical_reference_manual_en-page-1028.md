

```markdown
Chapter 28 I2S Controller (I2S)

GoBack

Figure 28.5-3. TDM PCM Standard Timing Diagram


28.5.4 PDM Standard

Under PDM standard, WS signal changes continuously during data transmission. The low-level and high-level of this signal indicates the left channel and right channel respectively. WS and SD signals change simultaneously. See Figure 28.5-4.

Figure 28.5-4. PDM Standard Timing Diagram


28.6 I2S TX/RX Clock

I2S_TX/RX_CLK is the master clock of I2S TX/RX unit, divided from:

• 40 MHz XTAL_CLK
• 120 MHz PLL_F120M_CLK
• 160 MHz PLL_F160M_CLK
• I2S_MCLK_in (external input clock)

The serial clock (BCK) of the I2S TX/RX unit is divided from I2S_TX/RX_CLK, as shown in Figure 28.6-1.
```