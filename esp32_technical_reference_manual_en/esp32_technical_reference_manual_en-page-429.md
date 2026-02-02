**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Figure Caption and Description:**
- **Figure 22.5-7:** Data Input by I2S DAC Interface

**Body Text:**
The I2S0 module should be configured to master transmitting mode when it connects to the on-chip DAC.

**Reference Figure Note:**
Figure 22.5-6 shows the signal connection between the I2SO module and the DAC.
The DAC's control module regards I2S_CLK as the clock in this configuration, As shown In Figure **22.5-7**, when the data bus inputs data to the DAC’s control module, the latter will input right-channel data to DAC1 module and left-channel data to DAC2 module.

When using the I2S DMA module, 8 bits of data-to-be-transmitted are shifted to the left by 8 bits of data-to-be-received into the DMA double-byte type of buffer.
The I2S_LCD_EN bit of register **I2S_CONF2_REG** should be set to 1; while **I2S_RX_SHORT_SYNC**, **I2S_TX_SHORT**, _SYNC, I2S_CONF_REG_, and **I2S_RX_MSB_SHIFT** and **I2S_TX_MSB SHIFT** shall all reset to O. The **I2S_TX_**

**Slave Mode bit of register i2s_CONF_REG** should be set to 0, as well when using the DAC mode of I2SO.
Select a suitable transmit mode according to the standards of transmitting a 16-bit digital data stream.

Configure the I2SO module clock to output a suitable frequency for **I2S_CLK** and the WS of i2s. Enable I2SO to send data after configuring the relevant DAC registers

**Subsection Title:**
22.6 I2S Interrupts

**Subsection Subtitle:**
22.6.1 FIFO Interrupts

**List Items (FIFO Interrupts):**
- **I2S_TX_HUNG_INT:** Triggered when transmitting data is timed out.
- **I2S_RX_HUNG_INT:** Triggered when receiving data is timed out.

- **I2S_TX_REMPY_INT:** Triggered when the transmit FIFO is empty. 

- **I2S_TX_WFULL_INT:** Triggered when the transmit FIFO is full

- **I2S_RX_REMPY_INT:** Triggered when the receive FIFO is empty.
  
- **I2S_RX_WFULL_INT:** Triggered when the receive FIFO is full.

- **I2S_TX_PUT_DATA_INT:** Triggered when the transmit FIFO is almost empty. 

- **I2S_RX_TAKE_DATA_INT:** Triggered when the receive FIFO is almost full

**Footer:**
Espressif Systems
429 ESP32 TRM (Version 5.6)
Submit Documentation Feedback