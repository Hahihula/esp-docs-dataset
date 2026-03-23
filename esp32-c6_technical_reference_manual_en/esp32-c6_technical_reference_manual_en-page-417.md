

```markdown
- HP_SLEEP
- LP_SLEEP
• Supports five preset power modes that suit various typical usage scenarios:
    - Active
    - Modem-sleep
    - Light-sleep0
    - Light-sleep1
    - Deep-sleep
• 16 KB SRAM
• 10 always-on (AON) registers
• RTC fast boot
• Programmable retention DMA to backup and restore the status of the CPU and peripherals when the chip switches between PMU states
• Supports a power controller that controls the power and clocks depending on the power modes

## 12.4 Functional Description

ESP32-C6’s low-power management involves the following components:

*   **Power scheme**: The power scheme of ESP32-C6 includes power regulators, digital power domains, analog power domains, etc.
*   **PMU controller**: It is the core part of PMU that controls the power up and down of the power domains, clocks, etc.
*   One RTC timer
*   10 always-on registers (LP_AON_STOREO_REG ~ LP_AON_STORE9_REG): These registers are always powered up and are not affected by any low-power modes, thus can be used for storing data that cannot be lost.
*   Eight LP GPIO pins (GPIO0 ~ GPIO7): These pins are always powered up and are not affected by any low-power modes, which makes them suitable for working as wake-up sources when the chip is in low-power modes. These pins can also work as regular GPIOs. For more information about the LP GPIOs, please refer to Chapter 7 IO MUX and GPIO Matrix (GPIO, IO MUX).
*   **16 KB SRAM**: The 16 KB SRAM is accessible to both HP CPU and LP CPU. It works under the HP CPU clock when accessed by the HP CPU and under the LP CPU clock when accessed by the LP CPU.
*   Brownout detector: It monitors the power of the supply voltage pins, ensuring stable chip operation and preventing the SoC from potential malfunction if subject to glitches or under voltage.

The following sections provide a detailed description of the components mentioned above.
```