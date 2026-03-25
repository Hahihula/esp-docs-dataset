

```markdown
Configure the PMU task to hold the HP pins before Deep-sleep. In Deep-sleep, the HP pins would be hold automatically by the PMU.

## 8.10 Hysteresis Characteristics

Each GPIO pin has hysteresis functionality. When hysteresis is not enabled, as shown in Figure 8.10-1, the level flip of the signal (C) input to the chip from the PAD has only one threshold (Vt, about 1.7 V). When the voltage on the PAD is higher than Vt, the level on the C is high. Otherwise, it is low. However, noise on the PAD may affect the signal on C.

![Figure 8.10-1. Example of Level Flip on the Chip Pad — Hysteresis Function Not Enabled](image)

When hysteresis is enabled, as shown in Figure 8.10-2, the level flip of C has two thresholds, high-level threshold (Vth, about 1.7 V) and low-level threshold (Vtl, about 1.4 V). When the voltage of pad goes from low to high, if the voltage is higher than Vth, the level of C is high. When the voltage of PAD goes from high to low, if the voltage is lower than Vtl, the level of C is low. When the voltage of PAD is between Vth and Vtl, the level of C does not change. The hysteresis function plays an anti-interference role by mitigating the impact of noise, consequently reducing the level flip time of C.

![Figure 8.10-2. Example of Level Flip on the Chip Pad — Hysteresis Function Enabled](image)

To enable the hysteresis function, follow the steps below:

*   `IO_MUX_GPIO[n]_HYS_SEL = 0` (n = 0~14, 23~28, corresponding to GPIO0~GPIO14, GPIO23~GPIO28)
    - Set EFUSE_HYS_EN_PAD to enable the hysteresis function for GPIO0~GPIO14 and GPIO23~GPIO28.
    - Or clear EFUSE_HYS_EN_PAD to disable the hysteresis function for GPIO0~GPIO14 and GPIO23~GPIO28.
*   `IO_MUX_GPIO[n]_HYS_SEL = 1` (n = 0~14, 23~28, corresponding to GPIO0~GPIO14, GPIO23~GPIO28)
```