**Chapter Title:**
Chapter 35 LED PWM Controller (LEDC)

**GoBack Link:** GoBack

---

**Register Section Header:**
Register 35.3. LEDC_CONF_REG (0x00D0)

**Field Description and Values Table for LEDC_CONF_REG:**

| Bit | Value |
|-----|-------|
| 1   | 0     |
| ... | ...   |

**Field Explanation - LEDC_APB_CLK_SEL:**
This field is used to select the common clock source for all the 4 timers.
- **Values:** 
  - `1`: APB_CLK
  - `2`: RC_FAST_CLK
  - `3`: XTAL_CLK

**Field Explanation - LEDC_CLK_EN:**
This bit is used to control clock. 
- **Values:**
  - `1`: Force clock on for register.
  - `0`: Support clock only when application writes registers.

---

**Register Section Header:**
Register 35.4. LEDC_CHn_HPOINT_REG (n: 0-7) (0x004+0x14*n)

**Field Description and Values Table for LEDC_CHn_HPOINT_REG:**

| Bit | Value |
|-----|-------|
| ... | ...   |

**Field Explanation - LEDC_HPPOINT_CHn:**
The output value changes to high when the selected timers has reached the value specified by this register.

---

**Register Section Header:**
Register 35.5. LEDC_CHn_DUTY_REG (n: 0-7) (0x008+0x14*n)

**Field Description and Values Table for LEDC_CHn_DUTY_REG:**

| Bit | Value |
|-----|-------|
| ... | ...   |

**Field Explanation - LEDC_DUTY_CHn:**
This register is used to change the output duty by controlling the Lpoint. The output value turns to low when the selected timers has reached the Lpoint.

---

**Footer Information:** 
Espressif Systems
Page Number 1321
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback