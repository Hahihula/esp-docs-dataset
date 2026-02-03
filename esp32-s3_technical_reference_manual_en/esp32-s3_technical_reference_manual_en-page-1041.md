**Title: Chapter 28 I2S Controller (I2S)**

- **64 x 32-bit RX FIFO**
- Compress/Decompress units

ESP32-S3 I2Sn module supports direct access (GDMA) to internal memory and external memory, see Chapter 3 GDMA Controller (GDMA).

Both the TX unit and the RX unit have a three-line interface that includes a bit clock line (BCK), a word select line (WS), and a serial data line (SD). The SD line of the TX unit is fixed as output, and the SD line of the RX unit as input. BCK and WS signal lines for TX unit and RX unit can be configured as master output mode or slave input mode.

The signal bus of I2Sn module is shown at the right part of Figure 28.4-1. The naming of these signals in RX and TX units follows the pattern: I2SnA_B_C, for example, I2sn1_BCK_in.

- **"A":** direction of data bus
- **"I":** input, receiving
- **"O":** output, transmitting

- **"B":** signal function
  - bit clock signal (BCK)
  - word select signal (WS)
  - serial data signal (SD)

- **"C":** signal direction
  - in: input signal into I2Sn module
  - out: output signal from I2Sn module

Table 28.4-1 provides a detailed description of I2Sn signals.

---

*Footer:*  
Espressif Systems  
Submit Documentation Feedback  

ESP32-S3 TRM (Version 1.7)