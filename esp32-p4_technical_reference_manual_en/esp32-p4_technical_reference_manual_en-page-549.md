

```markdown
Note:
In non-Deep-sleep mode, besides the above HP_SYSTEM registers, the LP_SYSTEM registers (LP_SYSTEM_REG_PAD_RTC_HOLD_CTRL0/1) can also control the Hold function for corresponding pins, with the same effect as the HP_SYSTEM registers.

• PMU_TIE_HIGH_HP_PAD_HOLD_ALL, controls the global Hold signal of all HP pins.

To use this feature, follow the steps below:

• To maintain the pin's input/output status in Deep-sleep, set LP_SYSTEM_REG_PAD_RTC_HOLD_CTRL0[n] (n = 16~31) or LP_SYSTEM_REG_PAD_RTC_HOLD_CTRL1[n] (n = 0~22) before powering down. To disable the hold function after waking up, clear both registers.

• To maintain the pin's input/output status in non-Deep-sleep mode, set HP_SYSTEM_GPIO_O_HOLD_LOW[n] (n = 0~31) or HP_SYSTEM_GPIO_O_HOLD_HIGH[n] (n = 0~6) before powering down. To disable the hold function after waking up, clear both registers. You can also use the LP_SYSTEM registers (LP_SYSTEM_REG_PAD_RTC_HOLD_CTRL0/1) as described above.

• Alternatively, set PMU_TIE_HIGH_HP_PAD_HOLD_ALL to maintain the input/output status of all HP pins and set PMU_TIE_LOW_HP_PAD_HOLD_ALL to disable the hold function for all HP pins.

• Alternatively, configure the PMU task to hold the HP pins before Deep-sleep. In Deep-sleep, the HP pins would be held automatically by the PMU.

LP Pins (GPIO0 ~ GPIO15):

The Hold state of each LP pin is controlled by the result of OR operation of the pin's Hold enable signal and the global Hold enable signal.

• Each pin's Hold enable signal is controlled by the following registers:

    - In Deep-sleep mode, LP_SYSTEM_REG_PAD_RTC_HOLD_CTRL0[n] (n = 0~15) controls the Hold signal of each pin of GPIO0~GPIO15.
    
    - In non-Deep-sleep mode, LP_IOMUX_LP_PAD_HOLD_REG[n] (n = 0~15) controls the Hold signal of each pin of GPIO0~GPIO15.

Note:
In non-Deep-sleep mode, besides the above LP_IOMUX register, the LP_SYSTEM register (LP_SYSTEM_REG_PAD_RTC_HOLD_CTRL0) can also control the Hold function for corresponding pins, with the same effect as the LP_IOMUX register.

• PMU_TIE_HIGH_LP_PAD_HOLD_ALL controls the global Hold signal of all LP pins.

To use this feature, follow the steps below:

• To maintain the pin's input/output status in Deep-sleep, set LP_SYSTEM_REG_PAD_RTC_HOLD_CTRL0[n] (n = 0~15) to hold the value of GPIO[n], or clear LP_SYSTEM_REG_PAD_RTC_HOLD_CTRL0[n] (n = 0~15) to disable the hold function of GPIO[n].

• To maintain the pin's input/output status in non-Deep-sleep mode, set LP_IOMUX_LP_PAD_HOLD_REG[n] (n = 0~15) to hold the value of GPIO[n], or clear
```