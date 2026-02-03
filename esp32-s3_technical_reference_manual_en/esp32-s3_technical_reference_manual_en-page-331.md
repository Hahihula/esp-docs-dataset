**Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

---

register RTC_I2C_INT_ENA_REG. Note that the bit map is shifted by 1. If a specific communication event is detected and its corresponding bit in register RTC_I2C_INT_ST_REG is set, the event can then be cleared using register RTC_I2C_INT_CLR_REG.

**2.7.4 RTC I2C Interrupts**

- RTC_I2C_SLAVE_TRAN_COMP_INT: Triggered when the slave finishes the transaction.
- RTC_I2C_ARBITRATION_LOST_INT: Triggered when the master loses control of the bus.
- RTC_I2C_MASTER_TRAN_COMP_INT: Triggered when the master completes the transaction.
- RTC_I2CTransComplete_INT: Triggered when a STOP signal is detected.
- RTC_I2CTimeOutInt: Triggered by time out event.
- RTC_I2CAckErrInt: Triggered by ACK error.
- RTC_I2CRxDataInt: Triggered when data is received.
- RTC_I2CTxDATA_INT: Triggered when data is transmitted.
- RTC_I2CDetectStartInt: Triggered when a START signal is detected.

---

**2.8 Address Mapping**

Table 2.8-1 shows the address mapping and available base registers for the peripherals accessible by ULP coprocessors.

| Peripheral(s) | Base Register | Main Bus Address | ULP-FSM Base | ULP-RISC-V Base |
|---------------|----------------|--------------------|--------------|------------------|
| RTC Control   | DR_REG_RTTCCNTL_BASE | 0x60008000 | 0x8000    | 0x8000           |
| RTC GPIO      | DR_REG_RTC_IO_BASE | 0x60008400 | 0x8400     | 0xA400           |
| ADC, Touch, TSENS | DR_REG_SENS_BASE | 0x60008800 | 0x8800    | 0xC800           |
| RTC I2C      | DR_REG_RTC_I2C_BASE | 0x60008C00 | 0x8C00     | 0xEC00           |

To find more information about registers for these peripherals, please check the following chapters.

---

**Table 2.8-2. Description of Registers for Peripherals Accessible by ULP Coprocessors**

| Registers Available for Peripherals | Described in Which Chapter |
|---------------------------------------|-------------------------------|
| Registers for RTC Control             | Chapter 10 Low-power Management (RTC_CNTL) |
| Registers for RTC GPIO                 | Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX) |
| Registers for ARC, Touch, TSENS       | Chapter 39 On-Chip Sensors and Analog Signal Processing |
| Registers for RTC I2C                  | Section 2.9 Register Summary in this chapter |

---

**2.9 Register Summary**

The following registers are used in ULP coprocessor:

Espressif Systems

ESP32-S3 TRM (Version 1.7)

Submit Documentation Feedback