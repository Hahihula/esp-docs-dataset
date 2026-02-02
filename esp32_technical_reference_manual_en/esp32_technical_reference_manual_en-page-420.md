**Chapter Title:**
Chapter 22 I2S Controller (I2S)

**Figure Caption and Diagram Description:**
- Figure caption: "PCM Standard"
- The diagram shows a waveform with labels BCK, WS, SD. It indicates the data flow in terms of MSB to LSB.

**Section Titles and Body Texts:**

1. **22.4.2 Module Reset**
   - The four low-order bits in register I2S_CONF_REG are described as follows:
     - `I2S_TX_RESET`
     - `I2S_RX_RESET`
     - `I2S_TX_FIFO_RESET`
     - `I2S_RX_FIFO_RESET`
   - These reset the receive module, transmit module and corresponding FIFO buffer respectively.
   - To finish a reset operation, set the bit in question then clear it by software.

2. **22.4.3 FIFO Operation**
   - The data read/write packet length for a FIFO operation is 32 bits with specific configurations:
     - `I2S_TX_DATA_NUM[5:0]`
     - `I2S_RX_DATA_NUM[5:0]`
   - These control the lengths of sent, received and buffered data.
   - Hardware inspects the received data length (`RX_LEN`) against transmitted data length (`TX_LEN`).
   - When `RX_LEN` exceeds `TX_LEN`, read out from FIFO to prevent overflow; otherwise continue feeding into FIFO.

3. **22.4.4 Sending Data**
   - The ESP32 I2S module performs a three-stage transmit operation:
     1. Read data from internal storage and transfer it to FIFO.
     2. Read data for transmission via FIFO.
     3. Clock out serially or in parallel as configured by the user.

**Footer:**
- "Espressif Systems"
- Page number: `420`
- Document version note: "ESP32 TRM (Version 5.6)"
- Links: Submit Documentation Feedback