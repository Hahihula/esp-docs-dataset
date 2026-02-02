**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**GoBack Link:** [GoBack](#)

---

**Section Heading:**

22.2 Features

**Subsection Subtitle:**
I2S mode

- Configurable high-precision output clock
- Full-duplex and half-duplex data transmit and receive modes
- Supports multiple digital audio standards
- Embedded A-law compression/decompression module
- Configurable clock signal
- Supports PDM signal input and output
- Configurable data transmit and receive modes

**Subsection Subtitle:**
LCD mode

- Supports multiple LCD modes, including external LCD
- Supports external Camera
- Supports on-chip DAC/ADC modes

**Subsection Subtitle:**
I2S interrupts

- Standard I2S interface interrupts
- I2S DMA interface interrupts

---

**Section Heading:**

22.3 The Clock of I2S Module

**Body Text:**
As is shown in Figure 22.3-1, I2Sn_CLK, as the master clock of I2S module, is derived from the 160 MHz clock PLL_F160M_CLK or the configurable analog output clock APLL_CLK. The serial clock (BCK) of the I2S module is derived from I2Sn_CLK. The I2S_CLKA_ENA bit of register I2S_CLKM_CONF_REG is used to select either PLL_F160M_CLK or APLL_CLK as the clock source for I2Sn. PLL_F160M_CLK is used as the clock source for I2Sn, by default.

**Notice:**
- When using PLL_F160M_CLK as the clock source, it is not recommended to divide it using decimals.
  For high performance audio applications, the analog PLL output clock source APLL_CLK must be used to acquire highly accurate I2Sn_CLK and BCK. For further details, please refer to the chapter entitled Reset and Clock.

- When ESP32 I2S works in slave mode, the master must use I2Sn_CLK as the master clock and f12s >= 8 * fack.

---

**Footer:**
Espressif Systems

**Page Number:** 
417

**Document Version:** 
ESP32 TRM (Version 5.6)

**Feedback Link:** [Submit Documentation Feedback](#)