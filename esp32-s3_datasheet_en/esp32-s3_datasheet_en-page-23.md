**Title: Pins**

---

### **2.3.2 RTC Functions**

When the chip is in Deep-sleep mode, the IO MUX described in Section [2.3.1 IO MUX Functions](#) will not work.
That is where the RTC IO MUX comes in. It allows multiple input/output signals to be a single input/output pin
in Deep-sleep mode, as the pin is connected to the RTC system and powered by VDDP3_RTC.

RTC IO pins can be assigned to RTC functions. They can

- Either work as RTC GPIOs (RTC_GPIO0, RTC_GPIO1, etc.), connected to the ULP coprocessor
- Or connect to RTC peripheral signals (sar_i2c_scl_0, sar_i2c_sda_0, etc.) - see Table 2-5 [RTC Peripheral Signals Routed via RTC IO MUX](#)

---

**Table:**

| Pin Function | Signal       | Description                    |
|--------------|-------------|--------------------------------|
| sar_i2c_scl | Serial clock | RTC I2C0/1 interface           |
| sar_i2c_sda | Serial data  |                               |

---

**Table Caption:** Table [2-5](#). RTC Peripheral Signals Routed via RTC IO MUX

---

**Table:**

| Pin No. | RTC Function Name | F0    | F1   | F2   | F3   |
|---------|-------------------|-------|------|------|------|
| 5       | RTC_GPIO0         | RTC_GPIO0 | sar_i2c_scl_0 |
| 6       | RTC_GPIO1         | RTC_GPIO1 | sar_i2c_sda_0 |
| ...     | ...               | ...    | ...   | ...   | ...   |

---

**Table Caption:** Table [2-6](#). RTC Functions

---

**Table:**

| Pin No. | RTC Function Name | F0    | F1    | F2    | F3    |
|---------|-------------------|-------|-------|-------|-------|
| 8       | RTC_GPIO3         | RTC_GPIO3 | sar_i2c_scl_1 |
| ...     | ...               | ...    | ...    | ...    | ...    |

---

**Table Caption:** Table [2-6](#). RTC Functions

---

This column lists the RTC GPIO names, since RTC functions are configured with RTC GPIO registers that use RTC GPIO numbering.

Regarding highlighted cells: see Section 2.3.4 Restrictions for GPIOs and RTC_GPIOs.

---

Espressif Systems  
Submit Documentation Feedback  

ESP32-S3 Series Datasheet v2.1

---