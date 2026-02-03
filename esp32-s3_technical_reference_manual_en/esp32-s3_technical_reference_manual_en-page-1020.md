**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**GoBack Link:** GoBack

---

**Register Information and Descriptions:**

1. **Register 27.7, I2C_SCL_STOP_HOLD_REG (0x0048)**
   - Description:
     ```
     I2C_SCL_STOP_HOLD_TIME
     This field is used to configure the delay after the STOP condition, in I2C module clock cycles.
     (R/W)
     ```
   - Binary Representation: 
     ```
     31 9 8 0 Reset
     ```

2. **Register 27.8, I2C_SCL_STOP_SETUP_REG (0x004C)**
   - Description:
     ```
     I2C_SCL_STOP_SETUP_TIME
     This field is used to configure the time between the rising edge of SCL and the rising edge of SDA, in I2C module clock cycles.
     (R/W)
     ```
   - Binary Representation: 
     ```
     31 (reserved) 9 8 Reset
     ```

3. **Register 27.9, I2C_SCL_ST_TIME_OUT_REG (0x0078)**
   - Description:
     ```
     I2C_SCL_ST_TO_I2C
     The maximum time that SCL_FSM remains unchanged.
     It should be no more than 23.
     (R/W)
     ```
   - Binary Representation: 
     ```
     31 5 4 0 Reset
     ```

---

**Footer Information:**  
Espressif Systems  
Submit Documentation Feedback

**Document Version and Title:**  
ESP32-S3 TRM (Version 1.7)