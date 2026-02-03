**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Note Section:**
The RTC I2C peripheral samples the SDA signals on the falling edge of SCL. If the slave changes SDA in less than 0.38 ms, the master may receive incorrect data.

**Section Title and Subtitle:**
2.7.3.3 I2C_WR - I2C Write Workflow

**Body Text (Preparation for RTC I2C write):**
- Configure RTC I2C instruction list, including instruction order, instruction code, and the data to be written in byte (byte_num). See the configuration of I2CO/I2CI in Section CMD_Controller in Chapter 27 [I2C Controller](#).
- Configure the slave register address by setting the register SENS_SAR_I2C_REG_ADDR, and the data to be transmitted in SENS_SAR_I2C_WDATA.
- Set SENS_SAR_I2C_START FORCE and SENS_SAR_I2C_START to start the transmission.
- Update the next data to be transmitted in SENS_SAR_I2C_WDATA, each time when an RTC_I2C_TX_DATA_INT interrupt is received.

**Body Text (I2C_WR instruction performs):**
The I2C_WR instruction performs the following operations:
1. Master generates a START signal.
2. Master sends slave addresss, with r/w bit set to 0 ("write"). Slave address is obtained from SENS_I2C_SLAVE_ADDRn.
3. Slave generates ACK.
4. Master sends slave register address.
5. Slave generates ACK.
6. Master generates a repeated START (RSTART) signal.
7. Master sends slave addresses, with r/w bit set to 0 ("write").
8. Master sends one byte of data.
9. Slave generates ACK. Master checks whether the number of transmitted bytes reaches the number set by the current instruction (byte_num). If yes, master jumps out of the write instruction and starts the next instruction. Otherwise the master repeats Step 8 and sends the next byte.
10. Master generates a STOP signal and stops the transmission.

**Figure Caption:**
Figure 2.7-2. I2C Write Operation

**Section Title (Next Section):**
2.7.3.4 Detecting Error Conditions

**Body Text for Next Section:**
Applications can query specific bits in the RTC_I2C_INT_ST_REG register to check if the transaction is successful. To enable checking for specific communication events, their corresponding bits should be set in Espressif Systems.

**Footer Information:**
ESP32-S3 TRM (Version 1.7) Page number at bottom center of page - "330" and options like Submit Documentation Feedback are present but not described as text content to extract from the image provided here, so they will be omitted in this transcription task based on instructions given for only extracting textual information without conversational context or descriptions beyond what is explicitly requested.