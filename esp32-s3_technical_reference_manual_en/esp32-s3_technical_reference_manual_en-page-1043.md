**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Section Header:**
28.5.1 TDM Philips Standard

**Body Text:**
Philips specifications require that WS signal changes one BCK clock cycle earlier than SD signal on BCK falling edge, which means that WS signal is valid from one clock cycle before transmitting the first bit of channel data and changes one clock before the end of channel data transfer. SD signal line transmits the most significant bit of audio data first.

Compared with Philips standard, TDM Philips standard supports multiple channels, see Figure 28.5-1.

**Figure Caption:**
Figure 28.5-1. TDM Philips Standard Timing Diagram

**Section Header:**
28.5.2 TDM MSB Alignment Standard

**Body Text:**
MSB alignment specifications require WS and SD signals change simultaneously on the falling edge of BCK. The WS signal is valid until the end of channel data transfer. The SD signal line transmits the most significant bit of audio data first.

Compared with MSB alignment standard, TDM MSB alignment standard supports multiple channels, see Figure 28.5-2.

**Figure Caption:**
Figure 28.5-2. TDM MSB Alignment Standard Timing Diagram

**Footer Information:**
Espressif Systems
1043 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback