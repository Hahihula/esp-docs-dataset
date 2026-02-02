**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Note:**
If more than 8 bits are requested, i.e., High - Low + 1 > 8, then the instruction will pad with zeros the bits above the eighth bit.

**Section Header:**
1.5 ULP Program Execution

**Body Text:**
The ULP coprocessor is designed to operate independently of the main CPUs, while they are either in deep sleep or running.
In a typical power-saving scenario, the ULP coprocessor operates while the main CPUs are in deep sleep. To save power even further, the ULP coprocessor can get into sleep mode as well. In such a scenario, there is a specific hardware timer in place to wake up the ULP coprocessor, since there is no software program running at the same time. This timer should be configured in advance by setting and then selecting one of the SENS_ULP_CP_SLEEP_CYCN_REG registers that contain the expiration period. This can be done either by the main program or the ULP program with the REG_WR and SLEEP instructions. Then, the ULP timer should be enabled by setting bit RTC_CNTL_ULP_CP_SLT_TIMER_EN in the RTC_CNTL_STATEO_REG register.

**Figure Caption:**
Figure 1.5-1. Control of ULP Program Execution

**Diagram Description (from left to right):**
SoC – Main CPUs
ULP-Coprocessor
ULP Timer

**Diagram Labels and Flow:**
- Wakeup SoC → Set Timer Period, Enable Timer on ULPCoprocessor/ULPTimer
- SLEEP/HALT → Run PC = SENS_PC_INIT (when the timer expires)

**Additional Information in Diagrams:**
- RTC_CNTL_ULP_CP_SLEEP_CYCN_REG is set to enable the ULP timer.
- The diagram shows a flow from "Enable" through various states like "Run," indicating that once enabled, it triggers an action.

**Body Text Continued:**
The ULP coprocessor puts itself into sleep mode by executing the HALT instruction. This also triggers the ULP timer to start counting RTC_SLOW_CLK ticks which, by default, originate from an internal 150 kHz RC oscillator. Once the timer expires, the ULP coprocessor is powered up and runs a program with the program counter.

**Footer:**
Espressif Systems
40 ESP32 TRM (Version 5.6)
Submit Documentation Feedback