**Title: Chapter 22 I2S Controller (I2S)**

---

### Figure Caption:
Figure 22.3-1. I2S Clock

---

**Body Text:**

The relation between `I2Sn_CLK` frequency \( f_{i2s} \) and the divider clock source frequency \( f_{pli} \) can be seen in the equation below:

\[ f_{i2s} = \frac{f_{pli}}{N + \frac{b}{a}} \]

- "N", whose value is >= 2, corresponds to the `REG_CLKM_DIV_NUM` [7:0] bits of register `I2S_CLKM_CONF_REG`.
- "b" is the `I2S_CLKM_DIV_B[5:0]` bit and "a" is the `I2S_CLKM_DIV_A[5:0]` bit.

In master mode, the serial clock BCK in the I2S module is derived from \( I2Sn_CLK \), that is:

\[ f_{BCK} = \frac{f_{i2s}}{M} \]

In master transmitting mode, "M", whose value is >= 2, is the `I2S_TX_BCK_DIV_NUM[5:0]` bit of register `I2S_SAMPLE`. In master receiving mode, "M" is the `I2S_RX_BCK_DIV_NUM[5:0]` bit of register `I2S_SAMPLE`. `_RATE_CONF_REG`.

---

**Subtitle:** 22.4 I2S Mode

**Body Text:**

The ESP32 I2S module integrates an A-law compression/decompression module to enable compression/decompression of the received audio data.

- The RX_PCM_BYPASS bit and the TX_PCM_BYPASS bit of register `I2S_CONF1_REG` should be cleared when using the A-law compression/decompression module.

---

**Subtitle:** 22.4.1 Supported Audio Standards

**Body Text:**

In the I2S bus, BCK is the serial clock, WS is the left-/right-channel selection signal (also called word select signal), and SD is the serial data signal for transmitting/receiving digital audio data.

- WS and SD signals in the I2S module change on the falling edge of `BCK`, while the SD signal can be sampled on the rising edge of BCK.
- If the `I2S_RX_RIGHT_FIRST` bit and the `I2S_TX_RIGHT_FIRST` bit of register `I2S_CONF_REG` are set to 1, the I2S module is configured to receive and transmit right-channel data first. Otherwise, the I2S module receives and transmits left-channel data first.

---

**Footer:**

Espressif Systems  
418  
ESP32 TRM (Version 5.6)  

[Submit Documentation Feedback](#)