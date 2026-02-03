**Chapter Title:**
Chapter 28 I2S Controller (I2S)

**Section Heading:**
28.9 Transmitting Data

**Note:**
Updating the configuration described in this and subsequent sections requires to set `I2S_TX_UPDATE` accordingly, to synchronize `I2Sn` TX registers from APB clock domain to TX clock domain.

For more detailed configuration, see Section 28.11.1.

In TX mode, I2Sn first reads data from DMA and sends these data out via output signals according to the configured data mode and channel mode.

**Subsection Heading:**
28.9.1 Data Format Control

**Body Text:**
Data format is controlled in the following phases:

- Phase I: read data from memory and write it to TX FIFO.
- Phase II: read the data to send (TX data) from TX FIFO and convert the data according to output data mode.

- Phase III: clock out the TX data serially.

**Subsection Heading:**
28.9.1.1 Bit Width Control of Channel Valid Data

**Body Text:**
The bit width of valid data in each channel is determined by `I2S_TX BITS MOD` and `I2S_TX_24 FILL EN`, see the table below.

**Table Title:**
Table 28.9-1. Bit Width of Channel Valid Data

| Channel Valid Data Width | I2S_TX BITS_MOD | I2S_TX_24 FILL_EN |
|---------------------------|-----------------|--------------------|
| 32                       | 31              | x^1                |
| 24                       | 23              | 1                  |
| 16                       | 23              | O                  |
| 8                        | 15              | X                  |

Note: `x` indicates this value is ignored.

**Subsection Heading:**
28.9.1.2 Endian Control of Channel Valid Data

**Body Text:**
When I2Sn reads data from DMA, the data endian under various data width is controlled by `I2S_TX BIG ENDIAN`, see the table below:

[The rest of this section appears to be cut off and not visible in the image.]

**Footer Information:**
Espressif Systems
1048 ESP32-S3 TRM (Version 1.7)

**Link Texts:**
Submit Documentation Feedback

**Navigation Link:** 
GoBack