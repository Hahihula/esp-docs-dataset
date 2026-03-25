

```markdown
Chapter 6 GPIO Matrix and IO MUX



Figure 6.10-1. Example of Level Flip on the Chip Pad — Hysteresis Function Not Enabled


When hysteresis is enabled, as shown in Figure 6.10-2, the level flip of C has two thresholds, high-level threshold (Vth, about 1.7 V) and low-level threshold (Vtl, about 1.4 V). When the voltage of PAD goes from low to high, if the voltage is higher than Vth, the level of C is high. When the voltage of PAD goes from high to low, if the voltage is lower than Vtl, the level of C is low. When the voltage of PAD is between Vth and Vtl, the level of C does not change. The hysteresis function plays an anti-interference role by mitigating the impact of noise, consequently reducing the level flip time of C.


Figure 6.10-2. Example of Level Flip on the Chip Pad — Hysteresis Function Enabled


To enable the hysteresis function, follow the steps below:

*   IO_MUX_GPIOn_HYS_SEL = 0 (n = 0~13, 22~29, corresponding to GPIO0~GPIO13, GPIO22~GPIO29)
    - Set EFUSE_HYS_EN_PAD to enable the hysteresis function for GPIOn.
    - Or clear EFUSE_HYS_EN_PAD to disable the hysteresis function for GPIOn.

*   IO_MUX_GPIOn_HYS_SEL = 1 (n = 0~13, 22~29, corresponding to GPIO0~GPIO13, GPIO22~GPIO29)
    - Set IO_MUX_GPIOn_HYS_EN to enable the hysteresis function for GPIOn.
    - Clear IO_MUX_GPIOn_HYS_EN to disable the hysteresis function for GPIOn.

Recommended Operation:

*   Set IO_MUX_GPIOn_HYS_SEL.
*   Then enable or disable the hysteresis function for GPIOn using IO_MUX_GPIOn_HYS_EN.



6.11 Power Supplies and Management of GPIO Pins
```