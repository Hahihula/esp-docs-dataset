**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Body Text:**
As shown in Table **22.4-3** and Figure **22.4-6**, at the second stage, the received data of the Rx unit is written into FIFO. There are four modes of writing received data into FIFO. Each mode corresponds to a value of I2S_RX_FIFO_MOD[2:0] bit.

**Table Title:**
Table 22.4-3. Modes of Writing Received Data into FIFO and the Corresponding Register Configuration

| Data format | Description |
|-------------|------------|
| **I2S_RX_FIFO_MOD[2:0]** | - |
| 0 | 16-bit dual channel data |
| 1 | 16-bit single channel data |
| 2 | 32-bit dual channel data |
| 3 | 32-bit single channel data |

**Figure Title and Description:**
Figure **22.4-6**: Modes of Writing Received Data into FIFO

At the third stage, CPU or DMA will read data from FIFO and write them into the internal memory directly. The register configuration that each mode corresponds to is shown in Table 22.4-4.

**Table Title:**
Table 22.4-4. The Register Configuration to Which the Four Modes Correspond

| I2S_RX_MSB_RIGHT | I2S_RX_CHAN_MOD | mode0 | mode1 | mode2 | mode3 |
|------------------|----------------|-------|-------|-------|-------|
| **0**            | -              |       |       |       |       |
| 0                 | left channel   | + right channel |    |     |      |
|                   |               |           |     |     |      |
| **1**             |                |         |     |     |      |
|                    |               |         |     |     |      |

**Footer:**
Espressif Systems  
423  
Submit Documentation Feedback

ESP32 TRM (Version 5.6)