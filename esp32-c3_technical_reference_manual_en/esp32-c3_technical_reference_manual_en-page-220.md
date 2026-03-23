

```markdown
modes (for details, please refer to Section 9.4.3), or can be used as regular GPIOs (for details, please refer to Chapter 5 IO MUX and GPIO Matrix (GPIO, IO MUX)).

• RTC fast memory: 8 KB SRAM that works under CPU clock (CPU_CLK), which can be used as extended memory.
• Voltage regulators: regulate the power supply to different power domains.

The schematic diagram of ESP32-C3's low-power management is shown in Figure 9.3-1.

Figure 9.3-1. Low-power Management Schematics

Note:
• For more information about different power domains, please check Section 9.4.1.
• Switches in the above diagram can be controlled by Register RTC_CNTL_DIG_PWC_REG.
• Signals in the above diagram are described below:

    - xpd_rtc_reg:
        * When RTC_CNTL_REGULATOR_FORCE_PU is set to 1, low power voltage regulator is always-on;
        * Otherwise, the low power voltage regulator is off when chip enters Light-sleep and Deep-sleep modes.
            In this case, the RTC domain is powered by an ultra low-power internal power source.

    - xpd_dig_reg:
        * When RTC_CNTL_DG_WRAP_PD_EN is enabled, the digital system voltage regulator is off when the chip enters Light-sleep and Deep-sleep modes;
        * Otherwise, the digital system voltage regulator is always-on.
```