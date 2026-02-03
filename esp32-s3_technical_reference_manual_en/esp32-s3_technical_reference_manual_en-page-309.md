**Title: Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

- **Instruction:** Set RTC_CNTL_UKP_SHUT_RESET_EN to reset ULP-RISC-V.

**Body Text:**
Enough time is reserved for the ULP-RISC-V to complete the operations above before it goes to halt. Figure 2.4-2 shows the relationship between the signals and register bits.

**Figure Caption:** 
Figure 2.4-2. Control of ULP Program Execution

**Diagram Description (from left to right, top to bottom):**
1. **SoC – Main CPU:**
   - WAKE
   - REG_WR
   
2. **ULP Timer:**
   - Enable RTC_CNTL_UKP_CP_SLP_TIMER_EN
   - Set Period RTC_CNTL_UKP_CP_TIMER_SLP_CYCLE

3. **ULP:**
   - HALT
   - Run PC = RTC_CNTL_UKP_CP_PC_INIT

4. **Enable Timer**

**Diagram Flow:** 
- The diagram shows a flow from the ULP Timer to SoC, indicating that when an Enable signal is received (RTC_CNTL_UKP_CP_SLP_TIMER_EN), it sets the period for the timer cycle and enables wake-up operations in both directions.

**Footer:**
Espressif Systems
309 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback