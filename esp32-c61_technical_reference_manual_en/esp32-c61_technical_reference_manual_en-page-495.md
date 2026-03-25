

```markdown
Chapter 11 Low-Power Management

- HP_MODEM
- HP_SLEEP
- LP_SLEEP

• Supports five preset power modes that suit various typical usage scenarios:
    - Active
    - Modem-sleep
    - Light-sleep0
    - Light-sleep1
    - Deep-sleep

• 10 always-on (AON) registers

• Programmable retention DMA to backup and restore the states of the CPU and peripherals when the chip switches between PMU states

• Supports a power controller that controls the power and clocks depending on the power modes

## 11.4 Functional Description

ESP32-C61’s low-power management involves the following components:

* Power scheme: includes power regulators, digital power domains, and analog power domains, etc.
* PMU controller: controls the power up and down of the power domains, clocks, etc. This is the core of PMU.
* One RTC timer
* 10 always-on registers (LP_AON_STOREO_REG ~ LP_AON_STORE9_REG): These registers are always powered up and are not affected by any low-power modes, thus can be used for storing data that cannot be lost.
* Eight LP GPIO pins (GPIO0 ~ GPIO7): These pins are always powered up and are not affected by any low-power modes, which makes them suitable for working as wake-up sources when the chip is in low-power modes. These pins can also work as regular GPIOs. For more information about the LP GPIOs, please refer to Chapter 6 GPIO Matrix and IO MUX.
* 320 KB HP SRAM: The 320 KB SRAM is accessible to CPU. It works under the CPU clock.
* Brownout detector: It monitors the power of the supply voltage pins, ensuring stable chip operation and preventing the SoC from potential malfunction if subject to glitches or under voltage.

The following sections provide a detailed description of the components mentioned above.

### 11.4.1 Power Scheme

Figure 11.4-1 shows the power scheme of ESP32-C61 that mainly includes:

• Two sets of regulators
```