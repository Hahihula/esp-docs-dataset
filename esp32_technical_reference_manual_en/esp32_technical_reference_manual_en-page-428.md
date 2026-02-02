Title: Chapter 22 I2S Controller (I2S)

Body Text:
I2S module. ESP32 supports signal inversion through the GPIO matrix. For details, please refer to the chapter about IO_MUX and the GPIO Matrix.

In order to make I2S work in camera mode, the I2S_LCD_EN bit and the I2S_CAMERA_EN bit of register I2S_CONF2

'REG are set to 1, the I2S_RX_SLAVE_MOD bit of register I2S_CONF_REG is set to 1, the I2S_RX_MSB_RIGHT bit and the I2S_RX_RIGHT_FIRST bit of I2S_CONF_REG are set to 0. Thus, I2S works in the LCD slave receiving mode. At the same time, in order to use the correct mode to receive data, both the I2S_RX_CHAN_MOD[2:0] bit of register I2S_CONF_CHAN_REG and the I2S_RX_FIFO_MOD[2:0] bit of register I2S_FIFO_CONF_REG are set to 1.

Subtitle: 22.5.3 ADC/DAC mode

Body Text:
In LCD mode, ESP32’s ADC and DAC can receive data. When the I2S0 module connects to the on-chip ADC, the I2S0 module should be set to master receiving mode. Figure **22.5-5** shows the signal connection between the I2S0 module and the ADC.

Image Caption:
Figure 22.5-5. ADC Interface of I2S0

Body Text (continued):
Firstly, the I2S_LCD_EN bit of register I2S_CONF_REG is set to 1, and the I2S_RX_SLAVE_MOD bit of register I2S_CONF_REG is set to 0, so that the I2S0 module works in LCD master receiving mode, and the I2S0 module clock is configured such that the WS signal of I2S0 outputs an appropriate frequency. Then, the SYSCON_SAR

ADC_DATA_TO_I2S bit of register SYSCON_APB_SARADC_CTRL_REG is set to 1. Enable I2S to receive data after configuring the relevant registers of SARADC. For details, please refer to Chapter **On-Chip Sensors and Analog Signal Processing**.

Image Caption:
Figure 22.5-6. DAC Interface of I2S

[The image shows a diagram with labels for "I2S0", "DAC controller", "DAC_CLK", "DAC1", "DAC2", "Data[7:0]", "Data1:", "Data2:", and arrows indicating data flow between components.]

Footer:
Espressif Systems
428 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

(Note: The text in the image is transcribed as it appears, including any typographical errors or inconsistencies.)