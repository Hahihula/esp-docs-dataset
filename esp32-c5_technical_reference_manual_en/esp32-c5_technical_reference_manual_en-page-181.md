

```markdown
Chapter 4 Low-Power CPU

GoBack

Figure 4.9-1. Wake-Up and Sleep Flow of LP CPU

- If the current power consumption state (clock, power supply, etc.) meets the requirements of the LP CPU, the PMU will immediately reply with the completion signal. Otherwise, it will adjust the power consumption state before replying with the completion signal.
- The wake-up module disables the STALL state of the LP CPU and enables interrupt receiving.
- The wake-up module starts the clock, releases reset (ignore this step if reset is not enabled for sleep), and starts working.

• Sleep process:
  - The LP CPU configures the register PMU_LP_CPU_SLEEP_REQ to enable the wake-up module to start the sleep process.
  - If PMU_LP_CPU_SLP_STALL_EN is 1, the wake-up module enables the STALL state of the LP CPU. If it is 0, the module does not enable that state.
  - The wake-up module waits for PMU_LP_CPU_SLP_STALL_WAIT LP CPU clock cycles, and then turns off the LP CPU clock. If PMU_LP_CPU_SLP_RESET_EN is 1, the module enables reset of the LP CPU.

Espressif Systems
Submit Documentation Feedback
ESP32-C5 TRM (Version 1.0)
```