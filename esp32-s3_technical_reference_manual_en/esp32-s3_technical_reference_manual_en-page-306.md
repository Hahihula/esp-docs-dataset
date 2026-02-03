**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**GoBack Link:** GoBack

---

**Table Title and Description:**
Table 2.2-1. Comparison of the Two Coprocessors

| Feature | ULP Coprocessors |
| --- | --- |
| **Memory (RTC Slow Memory)** | - |
| Work Clock Frequency | 8 KB |
| Wakeup Source | 17.5 MHz |
| Normal Mode | ULP Timer |
| After the chip is woken up: | Assist the main CPU to complete some tasks |

**Work Mode Table:**
- **Monitor Mode:** Retrieve data from sensors to monitor environment, when the chip is in sleep.
- **Control Low-Power Peripherals:** ADC1/ADC2
- **Touch Sensors**

**Additional Features for ULP-FSM and ULP-RISC-V:**
- RTC I2C (ULP-FSM)
- RTC GPIO (ULP-FSM)

**Architectural Details:**
- Architecture | Programmable FSM RISC-V

**Development Environment:** Special instruction set Standard C compiler

---

**Body Text Explanation:**
ULP coprocessor can access the modules in RTC domain via RTC registers. In many cases, the ULP coprocessor can be a good supplement to or replacement of the main CPU, especially for power-sensitive applications.

**Figure Description and Caption:** 
- **Figure 2.2-1 Diagram Title:**
  - APB BUS
  - ESP32-S3 RTC

**Diagram Components (from top-left clockwise):**
- ULP Timer -> ESP32-S3 RTC
- MUX -> ULP-RISC-V, ULP-FSM
- SAR CTRL -> MUX
- TSENS CTRL -> MUX
- ULP-FSM -> MUX
- ARBITER
  - RTC CNTL REG (ULP-FSM)
  - RTC IO REG (ULP-FSM)
  - I2C CTRL (ULP-FSM, ULP-RISC-V)
  - SARADC REG (ULP-RISC-V)

**Footer:**
Espressif Systems  
306 Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)