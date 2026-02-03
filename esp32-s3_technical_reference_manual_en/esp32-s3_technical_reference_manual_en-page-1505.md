**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**Link:**
GoBack

**Register Information (Hexadecimal Address):**
- **Address:** SENS_5AR_TOUCH_APPR_STATUS_REG (0x00E0)

**Diagram Description:**
A diagram showing the layout of various touch approach status registers with labels such as:
- SENS_TOUCH_SLP_APPROACH_PAD2_CNT
- SENS TOUCH APPROACH PAD1_CNT

**Register Details Table:**
| Bit 31 | ... | Bit 7 |
|--------|-----|-------|
| 0      |     | 0     |

**Description of Registers (RO - Read Only):**
- **SENS_TOUCH_APPROACH_PAD2_CNT:** Touch count of proximity pin 2.
- **SENS TOUCH APPROACH PAD1_CNT:** Touch count of proximity pin 1. 
- **SENS TOUCH APPROACH_PAD0_CNT:** Touch count of proximity pin 0.
- **SENS TOUCH SLP_APPROACH_CNT:** Touch count of sleep pin in proximity mode.

**Section Title:**
39.7.3 SENSOR (DIG_PERI) Registers

**Description for Section:**
The addresses in this section are relative to the [ADC controller base address] provided in Table 4.3-3 in Chapter 4 System and Memory.

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback