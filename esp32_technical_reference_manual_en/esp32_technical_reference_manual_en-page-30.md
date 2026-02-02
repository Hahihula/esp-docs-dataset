**Title: Chapter 1 ULP Coprocessor (ULP)**

---

### Figure Caption:
Figure 1.2-1. ULP Coprocessor Diagram

---

#### Section Title: 1.3 Functional Description

The text describes the functionality of an Ultra-Low Power coprocessor, which is a programmable FSM that can operate during deep sleep mode similar to general-purpose CPUs but with some special instructions for RTC controllers/ peripherals.

- The ULP coprocessor has:
  - Instructions useful in complex logic.
  - Special commands like HALT and JUMP.
  - Can access almost every module within the RTC domain through built-in instructions or RTC registers, often complementing CPU operations power-efficiently (Figure 1.2-1).

---

#### Section Title: 1.4 Instruction Set

The ULP coprocessor provides:
- Arithmetic and logic operations via ALU.
- Load and store data functions with LD, ST, REG_RD, and REG_WR instructions.

Additional capabilities include managing program execution through WAIT/HALT commands and controlling the sleep period of the ULP coprocessor using SLEEP instruction. 

---

**Footer:**
Espressif Systems  
30  
ESP32 TRM (Version 5.6)  

[Submit Documentation Feedback](#)