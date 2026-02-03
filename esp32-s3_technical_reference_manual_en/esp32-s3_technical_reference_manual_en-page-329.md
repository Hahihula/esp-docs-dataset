**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Section with List and Code Explanation:**
- READ: op_code = 2
- STOP: op_code = 3
- END: op_code = 4

**Note:** All slave addresses are expressed in 7 bits.

**Subsection Title (Red):**
2.7.3.2 I2C_RD - I2C Read Workflow

**Body Text with Preparation for RTC I2C read steps and references to other sections:**

1. Configure the instruction list of RTC I2C (see Section CMD_Controller in Chapter 27 I2C Controller (I2C)), including instruction order, instruction code, read data number (byte_num), and other information.
2. Configure the slave register address by setting the register SENS_SAR_I2C_REG_ADDR.
3. Start RTC I2C transmission by setting SENS_SAR_I2C_STARTFORCE and SENS_SAR_I2C_START.
4. When an RTC_I2C_RX_DATA_INT interrupt is received, transfer the read data stored in RTC_I2C_RDATA to SRAM RTC slow memory, or use the data directly.

**Body Text with Workflow Steps:**

The I2C_RD instruction performs the following operations (see Figure 2.7-1):

1. Master generates a START signal.
2. Master sends slave addresses, with r/w bit set to 0 (“write”). Slave address is obtained from SENS_I2C_SLAVER_ADDRn.
3. Slave generates ACK.
4. Master sends slave register address.
5. Slave generates ACK.
6. Master generates a repeated START (RSTART) signal.
7. Master sends slave addresses, with r/w bit set to 1 (“read”).
8. Slave sends one byte of data.
9. Master checks whether the number of transmitted bytes reaches the number set by the current instruction (byte_num). If yes, master jumps out of the read instruction and sends an NACK signal. Otherwise master repeats Step 8 and waits for the slave to send the next byte.
10. Master generates a STOP signal and stops reading.

**Figure Caption:**
Figure 2.7-1. I2C Read Operation

**Table Description (below Figure):**

| Master | Slave Address W | Reg Address | Slave Address R | Data(n) |
|--------|------------------|-------------|------------------|---------|
| START  |                  |             |                  |         |
| ACK    |                  |             |                  |         |

**Footer:**
Espressif Systems
329 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback