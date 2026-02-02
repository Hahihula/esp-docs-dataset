**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Section Header:**
1.6.1 Configuring RTC_I2C

**Body Text:**
Before the ULP coprocessor can use the I2C instruction, certain parameters of the RTC_I2C need to be configured. This can be done by the program running on one of the main CPUs, or by the ULP coprocessor itself. Configuration is performed by writing certain timing parameters into the RTC_I2C registers:

1. Set the low and high SCL half-periods by using `RTC_I2C_SCL_LOW_PERIOD_REG` and `RTC_I2C_SCL_HIGH_PERIOD_REG` in RTC_FAST_CLK cycles (e.g., RTC_I2C_SCL_LOW_PERIOD=40, RTC_I2C_SCL_HIGH_PERIOD=40 for 100 kHz frequency).
2. Set the number of cycles between the SDA switch and the falling edge of SCL by using `RTC_I2C_SDA_DUTY_REG` in RTC_FAST_CLK (e.g., RTC_I2C_SDA_DUTY=16).
3. Set the waiting time after the START condition by using `RTC_I2C_SCL_START_PERIOD_REG` (e.g., RTC_I2C_SCL_START_PERIOD=30).
4. Set the waiting time before the END condition by using `RTC_I2C_SCL_STOP_PERIOD_REG` (e.g., RTC_I2C_SCL_STOP_PERIOD=44).
5. Set the transaction timeout by using `RTC_I2C_TIMEOUT_REG` (e.g., RTC_I2C_TIMEOUT=200).
6. Enable the master mode (set the I2C_MS_MODE bit in `RTC_I2C_CTRL_REG`).
7. Write the address(es) of external slave(s) to `SENS_I2C_SLAVE_ADDRn` (n: 0-7). Up to eight slave addresses can be pre-programmed this way. One of these addresses can then be selected for each transaction as part of the ULP I2C instruction.

**Note:** Once RTC_I2C is configured, instructions `ULP_I2C_RD` and `I2C_WR` can be used.

**Section Header:**
1.6.2 Using RTC_I2C

**Body Text:**
The ULP coprocessor supports two instructions (with a single OpCode) for using RTC_I2C: `I2C_RD` (read) and `I2C_WR` (write).

**Subsection Title:**
1.6.2.1 I2C_RD - Read a Single Byte

**Body Text:**
The I2C_RD instruction performs the following I2C transaction:

1. Master generates a START condition.
2. Master sends slave address, with r/w bit set to 0 (“write”). Slave address is obtained from `SENS_I2C_SLAVE_ADDRn`, where n is given as an argument to the `I2C_RD` instruction.
3. Slave generates ACK.
4. Master sends slave register address (given as an argument to the I2C_RD instruction).
5. Slave generates ACK.
6. Master generates a repeat START condition.
7. Master sends slave address, with r/w bit set to 1 (“read”).
8. Slave sends one byte of data.
9. Master generates NACK.

**Footer:**
Espressif Systems
42

**Link Texts:**
- Submit Documentation Feedback
- ESP32 TRM (Version 5.6)