**Title: Chapter 1 ULP Coprocessor (ULP)**

**GoBack**

---

### Register 1.14. RTC_I2C_INT_EN_REG (0x028)

| Bit Position | Name                          |
|--------------|-------------------------------|
| 31           | RTC_I2C_TIME_OUT_INT_ENA     |
|              | Enable interrupt upon timeout.| (R/W) |
| 9            | RTC_I2C_TRANSComplete_INT_ENA |
|              | Enable interrupt upon detecting a stop pattern. | (R/W) |
| 8            | RTC_I2C_MASTER_TRANComp_INT_ENA |
|              | Enable interrupt upon completion of transaction, when in master mode. | (R/W) |
| 7            | RTC_I2C_ARBITRATION_LOST_INT_ENA |
|              | Enable interrupt upon losing control of the bus, when in master mode. | (R/W) |

---

### Register 1.15. RTC_I2C_INT_ST_REG (0x02c)

| Bit Position | Name                          |
|--------------|-------------------------------|
| 31           | RTC_I2C_TIME_OUT_INT_ST       |
|              | Detected timeout.             | (R/O) |
| 8            | RTC_I2C_TRANSComplete_INT_ST   |
|              | Detected stop pattern on I2C bus. | (R/O) |
| 7            | RTC_I2C_MASTER_TRANComp_INT_ST|
|              | Transaction completed, when in master mode. | (R/O) |
| 6            | RTC_I2C_ARBITRATION_LOST_INT_ST|
|              | Bus control lost, when in master mode. | (R/O) |

---

**Footer:**
- Espressif Systems
- Page number: 53
- Document version: ESP32 TRM (Version 5.6)
- Submit Documentation Feedback