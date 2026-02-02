**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** [GoBack](#)

**Body Text with Code Blocks, Headings, Tables, Lists as they appear in the image:**

- **Frequency of CW adjustment by register SENS_SAR_SW_FSTEP[15:0]:**
  ```
  freq = dig_clk_rtc_freq * SENS_SAR_SW_FSTEP/65536
  ```

- The frequency of `dig_clk_rtc` is typically 8 MHz.

- **Scaling Configuration:** 
  - Register `SENS_SAR_DAC_SCALE[1:0]`: the amplitude of a CW can be multiplied by values such as {1, 1/2, 1/4 or 1/8}.

- DC offset:
  - The offset may be introduced using register `SENS_SAR_DAC_DCn[7:0]`. This result will be saturated.
  
- **Phase shift:** 
  - A phase-shift of {0 / 90 / 180 / 270 degrees} can be added by setting the register `SENS_SAR_DAC_INVn[1:0]`.

**Figure Description and Caption (Figure 31.4-2):**
- **Caption:** Cosine Waveform (CW) Generator
- Diagram showing a CW generator with components labeled as follows:
  - dig_clk_rtc -> CW gen -> Scale -> Add DC -> Saturation -> Inverter -> cw_out[7:0]

**Subsection Title and Body Text:**

31.4.5 **DMA support**
- A DMA controller can be used to set the output of two DAC channels by configuring `SENS_SAR_DAC_DIG FORCE`, `I2S_clk` connected to DAC clk, and `I2S_DATA_OUT` for direct memory access.
- For more details refer to chapter DMA.

31.5 **Register Summary**
- Note: The registers listed below have been grouped according to their functionality; this particular grouping does not reflect the exact sequential order of place in memory.
- Abbreviations given under Column `Access` are explained in Section [Access Types for Registers](#).

**Subsection Title and Table (31.5.1 Sensors):**

31.5.1 **Sensors**
- | Name | Description | Address | Access |
  | --- | --- | --- | --- |
  | Touch pad setup and control registers | SENS_SAR_TOUCH_CTRL1_REG | Touch pad control | 0x3FF48858 R/W |

**Footer:**

Espressif Systems  
747 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback