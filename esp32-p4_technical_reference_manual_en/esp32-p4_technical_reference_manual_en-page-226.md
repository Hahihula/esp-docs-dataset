

```markdown
| Sleep | Wake-up flow Halt | Work Run (work) | Sleep flow | Sleep Halt |
|:-------|:-------------------|:-----------------|:-----------|:------------|
| Software |                  |                |           |            |
| Hardware | Wake up and send power-up request to PMU | Clear stall Enable intr Release reset | Start sleep flow Sets stall Disable intr Clk off Reset enable (Optional) Update LP state to IDLE |  |
| Stall | stall | unstash | stall unstall | PMU_LP_CPU_SLP_STALL_EN == 1<br>PMU_LP_CPU_SLP_STALL_EN == 0 |
| Interrupt | disable | enable | disable enable | PMU_LP_CPU_SLP_BYPASS_INTR_EN == 1<br>PMU_LP_CPU_SLP_BYPASS_INTR_EN == 0 |
| Reset | enable | disable | enable disable | PMU_LP_CPU_SLP_RESET_EN == 1<br>PMU_LP_CPU_SLP_RESET_EN == 0 |

Figure 3.10-1. Wake-Up and Sleep Flow of LP CPU

* The LP CPU will go through the wake-up process to start running
• Wake-up process:
    - The wake-up module receives a wake-up signal and sends a power-up request to the PMU.
    - If the current power consumption state (clock, power supply, etc.) meets the requirements of the LP CPU, the PMU will immediately reply with the completion signal. Otherwise, it will adjust the power consumption state before replying with the completion signal.
    - The wake-up module disables the STALL state of the LP CPU and enables interrupt receiving.
    - The wake-up module starts the clock, releases reset (ignore this step if reset is not enabled for sleep), and starts working.
• Sleep process:
    - The LP CPU configures the PMU_LP_CPU_SLEEP_REQ register to enable the wake-up module to start the sleep process.
    - If PMU_LP_CPU_SLP_STALL_EN is 1, the wake-up module enables the STALL state of the LP CPU. If it is 0, the module does not enable that state. If PMU_LP_CPU_SLP_BYPASS_INTR_EN is 1, the module masks all the LP CPU’s interrupts. If it is 0, the module does not mask them.
    - The wake-up module waits for PMU_LP_CPU_SLP_STALL_WAIT LP CPU clock cycles, and then turns off the LP CPU clock. If PMU_LP_CPU_SLP_RESET_EN is 1, the module enables reset of the LP CPU.
    - The wake-up module changes the state of the LP CPU to IDLE and the PMU can enter a deeper level of sleep state.
```