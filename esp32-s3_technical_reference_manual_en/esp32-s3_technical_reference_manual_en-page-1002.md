**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**Section Header with Code and Description:**
- **Code:** `I2C_SLAVE_STRETCH_INT_CLR` (slave) to clear interrupt, and set `I2C_SLAVE_SCL_STRETCH_CLR` (slave) to release the SCL line.
- After data transfer completes, I2Cmaster executes the STOP command, and generates an `I2C_TRANS_COMPLETE_INIT` (master) interrupt.

**Subsection Title:**
27.5.4 I2Cmaster Writes to I2Cslave with a 7-bit Address in Multiple Command Sequences

**Subsection Subtitle:**
27.5.4.1 Introduction

**Figure Caption and Description:**
- **Figure:** Figure 27.5-4, "I2Cmaster Writing to I2Cslave with a 7-bit Address in Multiple Sequences"
  
  The figure shows the process of writing data from an I2Cmaster to multiple segments (Segment0, Segment1, and Segment2) on an I2Cslave using command sequences. Each segment is represented by RAM addresses (`addr0`, `addr1`, etc.) with corresponding byte values being written.

**Body Text:**
Given that the I2C Controller RAM holds only 32 bytes, when data are too large to be processed even by the wrapped RAM, it is advised to transmit them in multiple command sequences. At the end of every command sequence is an END command. When the controller executes this END command to pull SCL low, software refreshes command sequence registers and the RAM for next transfer.

**Additional Information:**
- **Figure Caption:** Figure 27.5-4 shows how I2Cmaster writes to an I2C slave in two or three segments as an example.
- Once data is written into `I2Cmaster`'s RAM, it can be transferred via command sequences configured by Segment0.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback