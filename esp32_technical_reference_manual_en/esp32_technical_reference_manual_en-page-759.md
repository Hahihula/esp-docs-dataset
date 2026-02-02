**Title: Chapter 31 On-Chip Sensors and Analog Signal Processing**

**Subtitle: Register 31.23. SENS_SAR_DAC_CTRL2_REG (0xC09c)**

**Binary Diagram Description**
- The diagram shows a binary representation of the register with labels for each bit position from right to left, starting at '31' on the far left and ending at '0' in between various labeled fields such as "SENS_DAC_EN2", "SENS_DAC_CW_EN2", etc.

**Register Details:**
- **SENS_DAC_CW_EN2**: 1 selects CW generator as source for PDAC2_DAC[7:0], O: selects register reg_pdac2_dac[7:0] as source for PDAC2_DAC[7:0]. (R/W)
- **SENS_DAC_CW_EN1**: 1 selects CW generator as source for PDAC1_DAC[7:0], O: selects register reg_pdac1_dac[7:0] as source for PDAC1_DAC[7:0]. (R/W)
- **SENS_DAC_INV2**: DAC2, 0: does not invert any bits; 01: inverts all bits, 10: inverts MSB, 11: inverts all bits except for MSB. (R/W)
- **SENS_DAC_INV1**: DAC1, 00: does not invert any bits; 01: inverts all bits, 10: inverts MSB, 11: inverts all bits except for MSB. (R/W)
- **SENS_DAC_SCALE2**: DAC2, 00: no scale; 01: scale to 1/2; 10: scale to 1/4; 11: scale to 1/8. (R/W)
- **SENS_DAC_SCALE1**: DAC1, 00: no scale; 01: scale to 1/2; 10: scale to 1/4; 11: scale to 1/8. (R/W)
- **SENS_DAC_DC2**: DC offset for DAC2 CW generator. (R/W)
- **SENS_DAC_DC1**: DC offset for DAC1 CW generator. (R/W)

**Section Title:**
31.6.2 Advanced Peripheral Bus

**Body Text:**
The addresses in this section are relative to the base address of 0x6000_2600 (by AHB bus). The absolute register addresses are listed in Section **31.5.2 Advanced Peripheral Bus**.

For how to program reserved fields, please refer to Section [Programming Reserved Register Field](#).

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback