

```markdown
- LP_SLEEP
• Supports five preset power modes that suit various typical usage scenarios:
    - Active
    - Light-sleep0 (This mode does not power down the peripherals, but only the CPU. The clocks are not turned off. The power consumption is high, and the wake-up latency is short.)
    - Light-sleep1 (This mode does not power down the peripherals, but only turns off the clocks. The power consumption is relatively higher and the wake-up latency shorter.)
    - Light-sleep2 (This mode powers down the peripherals and needs data backup and restoration, resulting in lower power consumption and a longer wake-up latency.)
    - Deep-sleep
• LP SRAM (32 KB): Keep power up in all modes, can store HP CPU’s non-volatile data, and LP CPU’s instructions and data.
• Supports a programmable retention DMA that backs up and restores the CPU and peripherals status when the chip switches between PMU states.
• Supports a power controller that controls the power and clocks depending on the power modes.

## 14.4 Functional Description

ESP32-P4's low-power management involves the following components:

* **Power scheme**: The power scheme of ESP32-P4 includes power regulators, digital power domains, analog power domains, etc.
* **PMU controller**: It is the core part of the PMU, controlling the power up and down of power domains, clocks, etc.
* One RTC timer: For more information, please refer to Chapter 18 RTC Timer.
* 16 LP GPIO pins (GPIO0–GPIO15): These pins are always powered up and are not affected by any low-power modes, which makes them suitable for working as wake-up sources when the chip is in low-power modes. These pins can also work as regular GPIOs. For more information on LP GPIOs, refer to Chapter 9 GPIO Matrix and IO MUX.
* **32 KB SRAM**: The 32 KB SRAM is accessible to both HP CPU and LP CPU. It works under the HP CPU clock when accessed by the HP CPU and under the LP CPU clock when accessed by the LP CPU.
* **Brownout detector**: Monitors the power of the voltage supply pins, ensuring stable chip operation and preventing the SoC from potential malfunction if it is subject to glitches or under-voltage. For more information, refer to Chapter 23 Brown-out Detector.

The following sections provide a detailed description of the components mentioned above.

### 14.4.1 Power Scheme

Figure 14.4-1 shows the power scheme of ESP32-P4 that mainly includes:

* A DCDC voltage regulation feedback system
```