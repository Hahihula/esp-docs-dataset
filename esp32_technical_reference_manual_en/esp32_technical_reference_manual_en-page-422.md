**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**GoBack Link:** [GoBack](#)

---

**Table Description for I2S_TX_CHAN_MOD[2:0]**

| **Description** | |
| --- | --- |
| When I2S_TX_MSB_RIGHT equals 1, the left-channel data are "holding" their values and the right-channel data change into the left-channel data. | |
| Mono mode | |
| When I2S_TX_MSB_RIGHT equals 0, the left-channel data are constants in the range of REG[31:0]. | |
| When I2S_TX_MSB_RIGHT equals 1, the right-channel data are constants in the range of REG[31:0]. | |

---

**Section Title:** 
22.4.5 Receiving Data

**Body Text:**
The output of the third stage is determined by the mode of the I2S and I2S_TX BITS_MOD[5:0] bits of register I2S_SAMPLE_RATE_CONF_REG.

**Subsection Description for Receiving Data Phase in ESP32 I2S Module**

- The input serial-bit stream is transformed into a 64-bit parallel-data stream in I2S mode. In LCD mode, the input parallel-data stream will be extended to a 64-bit parallel-data stream.
- Received data are written into FIFO.
- Data are read from FIFO by CPU/DMA and written into the internal memory.

At the first stage of receiving data, the received-data stream is expanded to a zero-padded parallel-data stream with 32 high-order bits and 32 low-order bits, according to the level of the I2S_RX_WS_out (or I2Sn1_WS_in) signal. The I2S_RX_MSB_RIGHT bit of register I2S_CONF_REG is used to determine how the data are to be expanded.

**Figure Description:**
Figure 22.4-5 shows "The First Stage Of Receiving Data" with a diagram illustrating different stages (Data0, Data1, Data2) and their corresponding addresses in memory space for WS, SD, etc., including hexadecimal values like 0x7654, 0xFEDC, among others.

**Example Explanation:**
For example, as shown in Figure 22.4-5:
- If the width of serial data is 16 bits and I2S_RX_RIGHT_FIRST equals 1, Data0 will be discarded.
- When I2S_RX_MSB_RIGHT equals 1 or when I2S_RX_MSB_RIGHT equals 0: 
  - The first stage would contain {0x32100000, 0xFEDC0000}.
  - If the rightmost bit of Data0 is set to '1', it will be discarded.
- When I2S_RX_RIGHT FIRST equals 0:
  - Start receiving data from Data0.

**Example Values:**
If I2S_RX_MSB_RIGHT equals 1, first stage would contain {0xFEDC0000, 0x76540000}.
If I2S_RX_MSB_RIGHT equals 0, the first stage contains {0x76540000, 0xFEDC0000}.

**Footer:**
Espressif Systems  
ESP32 TRM (Version 5.6)  
Page number: 422

**Feedback Link:** [Submit Documentation Feedback](#)