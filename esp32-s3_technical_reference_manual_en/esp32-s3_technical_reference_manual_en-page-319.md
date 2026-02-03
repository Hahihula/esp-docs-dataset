**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Figure and Instruction Type Descriptions with Notes**

1. **Figure Caption:** Figure 2.5-14. Instruction Type - HALT

   **Description:** The instruction ends the operation of the ULP-FSM and puts it into power-down mode.

   **Note:**
   After executing this instruction, the ULP coprocessor wakeup timer gets started.
   
2. **Figure Caption:** Figure 2.5-15. Instruction Type - WAKE

   **Description:** This instruction sends an interrupt from the ULP-FSM to the RTC controller.

   - If the chip is in Deep-sleep mode, and the ULP wakeup timer is enabled, the above-mentioned interrupt will wake up the chip.
   - If the chip is not in Deep-sleep mode, and the ULP interrupt bit RTC_CNTL_ULP_CP_INT_ENA is set in register RTC_CNTL_INT_ENA_REG, an RTC interrupt will be triggered.

3. **Figure Caption:** Figure 2.5-16. Instruction Type - WAIT

   **Description:** The instruction will delay the ULP-FSM for a given number of cycles.
   
4. **Figure Caption:** Figure 2.5-17. Instruction Type - TSENS

**Subsection Titles and Descriptions**

- **2.5.2.8 WAKE – Wake up the Chip**
  
  (No additional text provided, just an instruction type figure)

- **2.5.2.9 WAIT – Wait for a Number of Cycles**
  
  (No additional text provided, but there is associated table with values: 31, 4; 28, 0; 27, 16; 15, 0)
  
- **2.5.2.10 TSENS – Take Measurement with Temperature Sensor**
  
  (No additional text provided, but there is associated table with values: 31, 10; 28, 2; 27, 16; 15, 0)

**Footer Information**

- **Page Number:** Page number not explicitly stated in the visible content.
  
- **Company Name and Document Version:** Espressif Systems
ESP32-S3 TRM (Version 1.7)
  
- **Action Links:**
   - Submit Documentation Feedback

(Note: The text provided is based on what can be seen from the image, including figure captions, descriptions of instructions types with notes where applicable.)