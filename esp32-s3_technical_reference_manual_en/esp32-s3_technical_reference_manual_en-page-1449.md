**Chapter Title:**
Chapter 38 Pulse Count Controller (PCNT)

**Section Header:**
Register 38.4, PCNT_CTRL_REG (0x0060)

**Body Text with Descriptions and Registers:**

- **PCNT_CNT_H_LIM_Un**: This register is used to configure the thr_h_lim value for unit n. (R/W)
  
- **PCNT_CNT_L_LIM_Un**: This register is used to configure the thr_l_lim value for unit n. (R/W)

**Register 38.4: PCNT_CTRL_REG (0x0060)**

| Bit | Description |
|-----|-------------|
| 15-0 | Reserved |

- **PCNT_PULSE_CNT_RST_Un**: Set this bit to clear unit n's counter. (R/W)
  
- **PCNT_CNT_PAUSE_Un**: Set this bit to freeze unit n's counter. (R/W)

- **PCNT_CLK_EN**: The registers clock gate enable signal of PCNT module.
  - `1`: the registers can be read and written by application
  - `0`: the registers cannot be read or written by application

**Register 38.5: PCNT_Un_CNT_REG (n = 0-3) (0x0030+0x4*n)**

| Bit | Description |
|-----|-------------|
| 16-0 | Reserved |

- **PCNT_PULSE_CNT_Un**: This register stores the current pulse count value for unit n. (RO)

**Footer:**
Espressif Systems
Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)