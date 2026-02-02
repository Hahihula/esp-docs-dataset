**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Figure Caption and Diagram Description:**
- **Figure 22.4-10:** PDM Receive Module

**Table Captions with Content:**
- Table 22.4-6 shows the configuration of the I2S_RX_PDM_SINC_DSR_16_EN bit whose PCM signal frequency remains 48 KHz at different PDM signal frequencies.
  
| PDM freq (KHz) | I2S_RX_PDM_SINC_DSR_16_EN | PCM freq (KHz) |
|-----------------|----------------------------|----------------|
| f_pcm×128       |                             |                |
| f_pcm×64        |                             | f_pcm         |

**Subsection Title:**
22.5 Camera-LCD Controller

**Body Text:**
There are three operational modes in the LCD mode of ESP32 I2S:
- LCD master transmitting mode
- Camera slave receiving mode
- ADC/DAC mode

The clock configuration of the LCD master transmitting mode is identical to I2S’ clock configuration. In the LCD mode, the frequency of WS is half of f_BCK.

In the ADC/DAC mode, use PLL_F160M_CLK as the clock source.

**Subsection Title:**
22.5.1 LCD Master Transmitting Mode

**Body Text and Figure Caption with Diagram Description:**
As shown in Figure 22.5-1, the WR signal of LCD connects to the WS signal of I2S. The LCD data bus width is 24 bits.

|                | Master                   | Slave         |
|----------------|--------------------------|---------------|
| I2S            | I2SnO_WS_out             | LCO          |
| I2S            | I2SnO_Data_out           | WR           |
|                 | SD                        |               |

**Figure Caption and Diagram Description:**
- **Figure 22.5-1:** LCD Master Transmitting Mode

The I2S_LCD_EN bit of register I2S_CONF2_REG needs to be set, the I2S_TX_SLAVE_MOD bit of register I2S_CONF_REG needs to be cleared in order to configure I2S to the LCD master transmitting mode.

Meanwhile, data should be sent under the correct mode, according to the I2S_TX_CHAN_MOD[2:0] bit of register I2S_CONF_CHAN_REG and the I2S_TX_FIFO_MOD[2:0] bit of register I2S_FIFO_CONF_REG. The WS signal needs to be inverted when it is routed through the GPIO Matrix.

**Footer Information:**
Espressif Systems
426 ESP32 TRM (Version 5.6)

**Navigation Links:**
- Submit Documentation Feedback