**Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**Section Title:**
31.6 Registers

**Subsection Title:**
31.6.1 Sensors

**Body Text:**
The addresses in this section are relative to (the RTC base address + 0x800) provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section 31.5.1 Sensors.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Table:**
- **Header:** 
  - SENS_SAR_READ_CTRL_REG (0x000)
  - SENS_SAR_DIG_FORCERE
  - SENS_SAR1 Sample Bit
  - SENS_SAR1 Sample Cycle
  - SENS_SAR1 CLK_DIV

- **Columns:**
  - Bits in the register, with binary representation and description:
    - Sens Sar Data Inv (0x80): Invert SAR ADC1 data. (R/W)
    - Sens Sar Dig Force (0x40): SAR ADC1 controlled by DIG ADC1 CTR; O: SAR ADC1 controlled by RTC ADC1 CTRL. (R/W)
    - Sens Sar Sample Bit Width of SAR ADC1, 00: for 9-bit, 01: for 10-bit, 10: for 11-bit, 11: for 12-bit. (R/W)
    - Sens Sar Sample Cycle Sample cycles for SAR ADC1. (R/W)
    - Sens Sar1 Clk Div Clock divider. (R/W)

**Additional Register Information:**
- **Register Title:** 
  - Register 31.2, SENS_ULP_CP_SLEEP_CYCO_REG (0x0018)

- **Description for the register:**
  - Sleep cycles for ULP coprocessor timer. (R/W)