**Title:**
Chapter 21 I2C Controller (I2C)

**Figure Title and Description:**
Figure 21.3-8. Master Writes to Slave with 7-bit Address in Three Segments

**Body Text:**

After detecting an I2C_END_DETECT_INT interrupt, the software can refresh the contents of the cmd and RAM blocks, as shown in the second segment. Subsequently, it should clear the I2C_ENDDetector_INT interrupt and resume the transaction by setting the I2CTrans_START bit. To stop the transaction, it should configure the cmd, as the third segment shows, and enable the I2CTrans_START bit to generate a STOP bit after detecting the I2C_END_DETECT_INT interrupt.

Please note that other masters on the bus will be starved of bus time between two segments. The bus is only released after a STOP signal is sent.

**Note:**
When there are more than three segments, the address of an END command in the cmd should not be altered into another command by the next segment.

**Footer Information:**

Espressif Systems
396 ESP32 TRM (Version 5.6)

**Link Texts:**
- GoBack
- Submit Documentation Feedback