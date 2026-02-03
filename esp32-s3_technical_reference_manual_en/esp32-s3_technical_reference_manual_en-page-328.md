**Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

---

### **2.7.2 Configuring RTC I2C**

Before ULP coprocessor can communicate using I2C instruction, RTC I2C need to be configured.
Configuration is performed by writing certain timing parameters into the RTC I2C registers. This can be done by the program running on the main CPU, or by the ULP coprocessor itself.

**Note:**
The timing parameters are configured in cycles of RTC_FAST_CLK running at 17.5 MHz.

1. Set the low and high SCL half-periods by configuring `RTC_I2C_SCL_LOW_PERIOD_REG` and `RTC_I2C_SCL_HIGH_PERIOD_REG` in RTC_FAST_CLK cycles (e.g., `RTC_I2C_SCL_LOW_PERIOD_REG = 40, RTC_I2C_SCL_HIGH_PERIOD_REG = 40` for 100 kHz frequency).

2. Set the number of cycles between the SDA switch and the falling edge of SCL by using `RTC_I2C_SDA_DUTY`. For example: `_REG in RTC_FAST_CLK (e.g., RTC_I2C_SDA_DUTY_REG = 16)`.

3. Set the waiting time after the START signal by using `RTC_I2C_SCL_START_PERIOD_REG` (e.g., `RTC_I2C_SCL_START_PERIOD = 30`).

4. Set the waiting time before the END signal by using `RTC_I2C_SCL_STOP_PERIOD_REG` (e.g., `RTC_I2C_SCL_STOP_PERIOD = 44`).

5. Set the transaction timeout by using `RTC_I2C_TIME_OUT_REG` (e.g., `RTC_I2C_TIME_OUT_REG = 200`).

6. Configure the RTC I2C controller into master mode by setting the bit `RTC_I2C_MS_MODE` in `RTC_I2C_CTRL`.

7. Configure the address(es) of external slave(s):
   - If ULP-RISC-V or main CPU is used, then write the slave address to `SENS_SAR_I2C_SLAVE_ADDR`.
   - If ULP-FSM is used, then write the slave address to `SENS_I2C_SLAVE_ADDRn` (where n: 0-7).
   
Up to eight slave addresses can be pre-programmed. One of these addresses can then be selected for each transaction as part of the RTC I2C instruction.

Once RTC I2C is configured, the main CPU or the ULP coprocessor can communicate with the external I2C devices.

---

### **2.7.3 Using RTC I2C**

#### 2.7.3.1 Instruction Format

The format of RTC I2C instruction is basically consistent with that of I2C0/I2C1, see Section [I2C CMD Controller](Chapter 27 I2C Controller (I2C)) except the following:

- RTC I2C has different op_code mapping:
  - RSTART: op_code = 0
  - WRITE: op_code = 1

---

**Espressif Systems**

**Page Number:** 328  
**Document Version:** ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)