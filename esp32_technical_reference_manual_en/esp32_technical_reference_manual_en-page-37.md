**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Section Header with Subtitle and Description:**
1.4.9 Sleep – Set the ULP Timer’s Wake-up Period

- **Description:** This instruction sends an interrupt from the ULP coprocessor to the RTC controller.
  - If SoC is in Deep-sleep mode, and the ULP wake-up is enabled, this will trigger a wake up of the SoC.

**Table:**
| Operand | Description |
|---------|-------------|
| 31      | see Figure 1.4-12. Instruction Type — SLEEP |

**Figure Caption:** 
Figure 1.4-12. Instruction Type — SLEEP

**Description for Figure (continued):**
sleep_reg selects one of five SENS_ULP_CP_SLEEP_CYCn_REG values to set the wake-up period.

**Subsection Header:**
1.4.10 WAIT – Wait for a Number of Cycles

- **Description:** The instruction waits between sleeps.
  - This will delay the ULP coprocessor from getting into sleep mode by waiting for specified cycles before resuming operation after each cycle wait event (e.g., ADC interrupt).

**Table:**
| Operand | Description |
|---------|-------------|
| Cycles  | see Figure 1.4-13 |

**Figure Caption:** 
Figure 1.4-13. Instruction Type — WAIT

**Subsection Header:**
1.4.11 ADC – Take Measurement with ADC

- **Description:** This instruction will delay the ULP coprocessor from getting into sleep mode for a certain number of cycles.
  - The selected ADC channel (0 = SAR ADC1, 1 = SAR ADC2) is used to take measurements.

**Table:**
| Operand | Description |
|---------|-------------|
| Rdst    | Destination Register R[0-3], results will be stored in this register. |

**Figure Caption:** 
Figure 1.4-14. Instruction Type — ADC

**Subsection Header (continued):**
Sar Mux
- SARADC Pad [Sar_Mux - 1] is enabled, see Table 1.4-4.

**Footer:**
Espressif Systems  
37  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback