**Title: Functional Description**

---

| Interface | Signal | Pin | Function |
|-----------|--------|-----|----------|
| LED PWM | ledc_hs_sig_out0~7 | Any GPIO Pins | 16 independent channels @80 MHz clock/RTC CLK. Duty accuracy: 16 bits. |
|          | ledc_ls_sig_out0~7 |     |          |
|          | I2SOI_DATA_in0~15 |     |          |
|          | I2SOO_BCK_in |     |          |
|          | I2SO0_WS_in |     |          |
|          | I2SO0_BCK_in |     |          |
|          | I2SO1_WS_in |     |          |
|          | I2SO1_H_SYNC |     |          |
|          | I2SO1_V_SYNC |     |          |
|          | I2SO1_ENABLE |     |          |
|          | I2SO0_BCK_out |     |          |
|          | I2SO0_WS_out |     |          |
|          | I2SO1_BCK_out |     |          |
|          | I2SOI_WS_out |     |          |
|          | I2SOO_DATA_out0~23 | Any GPIO Pins | Stereo input and output from/to the audio codec; parallel LCD data output; parallel camera data input. |

**Note:** 
- I2S0_CLK and I2S1_CLK can only be mapped to GPIO0, UORXD (GPIO3), or UOTXD (GPIO1) via IO MUX by selecting GPIO functions CLK_OUT1, CLK_OUT2, and CLK_OUT3.
- For more information:
  - ESP32 Technical Reference Manual
  - Chapter I0_MUX and GPIO Matrix > Table IO MUX Pad Summary.

---

| Interface | Signal | Pin | Function |
|-----------|--------|-----|----------|
| I2S | S1I_DATA_in0~15 | Any GPIO Pins |          |

**General Purpose**

- **SPI**
  - HSPI_Q_in/_out
  - HSPIO_ID_in/_out
  - HSPICLK_in/_out
  - HSPICSO_in/_out
  - VSPI_Q_in/_out
  - VSPID_in/_out
  - VSPICLK_in/_out
  - VSPICSO_in/_out

**General Purpose**

- **SPI**
  - Both master and slave modes;
  - Four sub-modes of the SPI transfer format;
  - Configurable SPI frequency;
  - Up to 64 bytes of FIFO and DMA.

---

| Interface | Signal | Pin | Function |
|-----------|--------|-----|----------|
| RMT | RMT_SiG_IN0~7 | Any GPIO Pins | Eight channels for an IR transmitter and receiver of various waveforms. |

**General Purpose**

- **SPI**
  - Standard SPI consists of clock, chip-select, MOSI and MISO.
  - These SPIs can be connected to LCD and other external devices.

---

Espressif Systems  
49  
ESP32 Series Datasheet v5.2

Submit Documentation Feedback