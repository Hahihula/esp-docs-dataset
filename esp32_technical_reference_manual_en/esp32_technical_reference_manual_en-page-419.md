**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Section Titles and Subsections with Content:**

1. **22.4.1 Philips Standard**
   - Figure Caption:
     - "Figure 22.4-1. Philips Standard"
   - Body Text:
     - As is shown in Figure 22.4-1, the Philips I2S bus specifications require that the WS signal starts to change one BCK clock cycle earlier than the SD signal on BCK falling edge, which means the WS signal becomes valid one clock cycle before the first bit of data transfer on the current channel, and changes one clock cycle earlier than the end of data transfer on the current channel. The SD signal line transmits the most significant bit of audio data first. If the I2S_RX_MSB_SHIFT bit and the I2S_TX_MSB_SHIFT bit of register I2S_CONF_REG are set to 1, respectively, the I2S module will use the Philips standard when receiving and transmitting data.

2. **22.4.1.2 MSB Alignment Standard**
   - Figure Caption:
     - "Figure 22.4-2. MSB Alignment Standard"
   - Body Text:
     - The MSB alignment standard is shown in Figure 22.4-2. WS and SD signals both change simultaneously on the falling edge of BCK under the MSB alignment standard. The WS signal continues until the end of the current channel-data transmission, and the SD signal line transmits the most significant bit of audio data first. If the I2S_RX_MSB_SHIFT and I2S_TX_MSB_SHIFT bits of register I2S_CONF_REG are cleared, the I2S module will use the MSB alignment standard when receiving and transmitting data.

3. **22.4.1.3 PCM Standard**
   - Figure Caption:
     - "Figure 22.4-3"
   - Body Text:
     - As is shown in Figure 22.4-3, under the short frame synchronization mode of the PCM standard, the WS signal starts to change a BCK clock cycle earlier than the SD signal, which means that the WS signal takes effect a clock cycle earlier than the first bit of the current channel-data transmission and continues for one extra BCK clock cycle. The SD signal line transmits the most significant bit of audio data first. If the I2S_RX_SHORT_SYNC and I2S_TX_SHORT_SYNC bits of register I2S_CONF_REG are set, the I2S module will receive and transmit data in the short frame synchronization mode.

**Footer:**
- "Espressif Systems"
- Page Number:
  - "419 ESP32 TRM (Version 5.6)"
- Link Texts:
  - "Submit Documentation Feedback"