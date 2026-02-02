**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Body Text:**

about IO_MUX and the GPIO Matrix.
The I2S_LCD_TX_SDX2_EN bit and the I2S_LCD_TX_WRX2_EN bit of register I2S_CONF2_REG should be set to the LCD master transmitting mode, so that both the data bus and WR signal work in the appropriate mode.

**Figure Captions:**
- Figure 22.5-2. LCD Master Transmitting Data Frame, Form 1
- Figure 22.5-3. LCD Master Transmitting Data Frame, Form 2

**Subsection Title with Numbering:**
22.5.2 Camera Slave Receiving Mode

**Body Text under Subsection:**

ESP32 I2S supports a camera slave mode for high-speed data transfer from external camera modules. As shown in Figure 22.5-4, in this mode, I2S is set to slave receiving mode. Besides the 16-channel data signal bus I2SnData_in, there are other signals, such as I2SnH_SYNC, I2SnV_SYNC and I2SnH_ENABLE.

The PCLK in the Camera module connects to I2SnWS_in on the I2S module, as Figure 22.5-4 shows.
**Figure Caption:**
- Figure 22.5-4. Camera Slave Receiving Mode

**Additional Information under Subsection:**

When I2S is in the camera slave receiving mode, and when I2SnH_SYNC, I2S_V_SYNC and I2S_H_REF are held high, the master starts transmitting data, that is,

`transmission_start = (I2SnH_SYNC == 1) &&(I2SnV_SYNC == 1) &&(I2SnH_ENABLE == 1)`

Thus, during data transmission, these three signals should be kept at a high level. For example, if the I2SnV_SYNC signal of a camera is at low level during data transmission, it will be inverted when routed to the

**Footer:**
Espressif Systems
427 ESP32 TRM (Version 5.6)
Submit Documentation Feedback