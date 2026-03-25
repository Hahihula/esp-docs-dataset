

```markdown
Chapter 13 Low-Power Management

- HP_SLEEP
- LP_SLEEP

* Supports five preset power modes that suit varying typical usage scenarios:
    - Active
    - Modem-sleep
    - Light-sleep0
    - Light-sleep1
    - Deep-sleep

• 16 KB SRAM (LP SRAM)
• 10 always-on (AON) registers
• RTC fast boot
• Supports a programmable retention DMA that backs up and restores the CPU and peripherals status when the chip switches between PMU states.
• Supports a power controller that controls the power and clocks depending on the power modes

## 13.4 Functional Description

ESP32-C5's low-power management involves the following components:

* **Power scheme**: The power scheme of ESP32-C5 includes power regulators, digital power domains, analog power domains, etc.
* PMU controller: It is the core part of PMU that controls the power up and down of the power domains, clocks, etc.
* One RTC timer: For more information, please refer to Chapter 17 RTC Timer.
* **10 always-on registers (LP_AON_STORE0_REG ~ LP_AON_STORE9_REG)**: These registers are always powered up and are not affected by any low-power modes, thus can be used for storing data that should not be lost.
* Seven LP GPIO pins (GPIO0 ~ GPIO6): These pins are always powered up and are not affected by any low-power modes, which makes them suitable for working as wake-up sources when the chip is in low-power modes. These pins can also work as regular GPIOs. For more information about the LP GPIOs, please refer to Chapter 8 GPIO Matrix and IO MUX.
* **LP SRAM**: The 16 KB SRAM is accessible to both HP CPU and LP CPU. It works under the HP CPU clock when accessed by the HP CPU and under the LP CPU clock when accessed by the LP CPU.

The following sections provide a detailed description of the components mentioned above.

### 13.4.1 Power Scheme

Figure 13.4-1 shows the power scheme of ESP32-C5 that mainly includes:

* Two regulators
```