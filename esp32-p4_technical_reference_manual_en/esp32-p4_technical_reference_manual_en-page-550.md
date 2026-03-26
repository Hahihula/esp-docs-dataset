

```markdown
LP_IOMUX_LP_PAD_HOLD_REG[n] (n = 0~15) to disable the hold function of GPIO[n]. You can also use the LP_SYSTEM register (LP_SYSTEM_REG_PAD_RTC_HOLD_CTRL0) as described above.
* Alternatively, set PMU_TIE_HIGH_LP_PAD_HOLD_ALL to hold the values of all LP pins, and set PMU_TIE_LOW_LP_PAD_HOLD_ALL to disable the hold function of all LP pins.
* Alternatively, configure the PMU task to hold LP pins before Deep-sleep. In Deep-sleep, LP pins will be hold automatically by the PMU.

## 9.10 Hysteresis Characteristics of GPIO Pins

Each GPIO pin has hysteresis functionality. When hysteresis is not enabled, as shown in Figure 9.10-1, the level flip of the signal (C) input to the chip from the PAD has only one threshold (Vt, about 1.7 V). When the voltage on the PAD is higher than Vt, the level on the C is high. Otherwise, it is low. However, noise on the PAD may affect the signal on C.

![Figure 9.10-1. Example of Level Flip on the Chip Pad — Hysteresis Function Not Enabled](image)

When hysteresis is enabled, as shown in Figure 9.10-2, the level flip of C has two thresholds, high-level threshold (Vth, about 1.7 V) and low-level threshold (Vtl, about 1.4 V). When the voltage of pad goes from low to high, if the voltage is higher than Vth, the level of C is high. When the voltage of PAD goes from high to low, if the voltage is lower than Vtl, the level of C is low. When the voltage of PAD is between Vth and Vtl, the level of C does not change. The hysteresis function plays an anti-interference role by mitigating the impact of noise, consequently reducing the level flip time of C.

To enable the hysteresis function, follow the steps below:
* Set LP_IOMUX_LP_GPIO_HYS[n] (n ranges from 0 ~ 15, corresponding to GPIO0 ~ GPIO15), HP_SYS_GPIO0_HYS_LOW[n] (n ranges from 0 ~ 31, corresponding to GPIO16 ~ GPIO47) or HP_SYS_GPIO0_HYS_HIGH[n] (n ranges from 0 ~ 6, corresponding to GPIO48 ~ GPIO54) to 1 to enable the hysteresis function for GPIO[n].
* Set LP_IOMUX_LP_GPIO_HYS[n] (n ranges from 0 ~ 15, corresponding to GPIO0 ~ GPIO15), HP_SYS_GPIO0_HYS_LOW[n] (n ranges from 0 ~ 31, corresponding to GPIO16 ~ GPIO47) or HP_SYS_GPIO0_HYS_HIGH[n] (n ranges from 0 ~ 6, corresponding to GPIO48 ~ GPIO54) to 0 to disable the hysteresis function for GPIO[n].
```