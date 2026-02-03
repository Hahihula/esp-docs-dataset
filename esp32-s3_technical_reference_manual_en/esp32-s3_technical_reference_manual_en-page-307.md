**Title: Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

---

### Section Title:
2.3 Programming Workflow

**Body Text:**
The ULP-RISC-V is intended for programming using C language. The program in C is then compiled to RV32IMC standard instruction code. The ULP-FSM is using custom instructions normally not supported by high-level programming language. Users develop their programs using ULP-FSM instructions (see Section 2.5.2).

**Diagram Description:**
- **Figure Caption:** Figure 2.3-1. Programming Workflow
- Diagram shows the workflow from User to Compiler, then Instruction Set RV32IMC and ULP-RISC-V, back to User with another set of Instruction Code.

---

### Section Title:
2.4 ULP Coprocessor Sleep and Wake-Up Workflow

**Body Text:**
ULP coprocessor is designed to operate independently of the CPU, while the CPU is either in sleep or running.
In a typical power-saving scenario, the chip goes to Deep-sleep mode to lower power consumption. Before setting the chip to sleep mode, users should complete the following operations.

1. Flash the program to be executed by ULP coprocessor into RTC slow memory.
2. Select the working ULP coprocessor by configuring RTC_CNTL_COCPU_SEL:
   - 0: select ULP-RISC-V
   - 1: select ULP-FSM
3. If ULP-RISC-V is selected as a working ULP coprocessor, please set and reset RTC_CNTL_COCPU_CLKFO;
4. Set sleep cycles for the timer by configuring RTC_CNTL_ULP_CP_TIMER_1_REG.
5. Enable the timer by software or by RTC GPIO;

**Additional Information:**
- By software: set RTC_CNTL_ULP_CP_SLP_TIMER_EN.

---

**Footer:** 
Espressif Systems  
307  
ESP32-S3 TRM (Version 1.7)  

**Link Texts:**
- Submit Documentation Feedback
- GoBack