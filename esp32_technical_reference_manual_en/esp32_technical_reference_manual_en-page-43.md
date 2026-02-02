**Chapter Title: ULP Coprocessor (ULP)**

---

### Figure Caption:
- **Figure 1.6-1. I2C Read Operation**

| Master | Slave Address W | Reg Address | RST | Slave Address R | ACK | Data |
|--------|-----------------|-------------|-----|------------------|-----|------|
| ACK    |                 |             |     |                 |     | STOP |

**Note:**
The RTC_I2C peripheral samples the SDA signals on the falling edge of SCL. If the slave changes SDA in less than 0.38 microseconds, the master will receive incorrect data.
The byte received from the slave is stored into the RO register.

---

#### Subtitle:
1.6.2.2 I2C_WR - Write a Single Byte

**Body Text:**
The I2C_WR instruction performs the following I2C transaction (see Figure 1.6-2):

1. Master generates a START condition.
2. Master sends slave addresses, with r/w bit set to 0 ("write"). Slave address is obtained from `SENS_I2C_SLAVE_ADDRn`, where `n` is given as an argument to the I2C_WR instruction.
3. Slave generates ACK.
4. Master sends slave register address (given as an argument to the I2C_WR instruction).
5. Slave generates ACK.
6. Master generates a repeated START condition.
7. Master sends slave addresses, with r/w bit set to 0 ("write").
8. Master sends one byte of data.
9. Slave generates ACK.
10. Master generates a STOP condition.

---

#### Subtitle:
1.6.2.3 Detecting Error Conditions

**Body Text:**
ULP I2C_RD and I2C_WR instructions will not report error conditions, such as a NACK from a slave, via ULP registers. Instead, applications can query specific bits in the `RTC_I2C_INT_ST_REG` register to determine if the transaction was successful. To enable checking for specific communication events, their corresponding bits should be set in register `RTC_I2C_INT_EN_REG`. Note that the bit map is shifted by 1. If a specific communication event is detected and set in register `RTC_I2C_INT_ST_REG`, it can then be cleared using `RTC_I2C_INT_CLR_REG`.

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32 TRM (Version 5.6)