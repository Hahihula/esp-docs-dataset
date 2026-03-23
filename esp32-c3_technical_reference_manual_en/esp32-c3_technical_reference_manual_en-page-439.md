
```markdown
Register 16.8. SYSTEM_CPU_PER_CONF_REG (0x0008)

SYSTEM_CPUREIOD_SEL    Set this field to select the CPU clock frequency. For details, please refer to Table 6.2-3 in Chapter 6 Reset and Clock.(R/W)

SYSTEM_PLL_FREQ_SEL    Set this bit to select the PLL clock frequency. For details, please refer to Table 6.2-3 in Chapter 6 Reset and Clock. (R/W)

SYSTEM_CPU_WAIT_MODE_FORCE_ON   Set this bit to force on the clock gate of CPU wait mode.
Usually, after executing the WFI instruction, CPU enters the wait mode, during which the clock gate of CPU is turned off until any interrupts occur. In this way, power consumption is saved. However, if this bit is set, the clock gate of CPU is always on and will not be turned off by the WFI instruction. (R/W)

SYSTEM_CPU_WAITI_DELAY_NUM   Sets the number of delay cycles to turn off the CPU clock gate after the CPU enters the wait mode because of a WFI instruction. (R/W)


Register 16.9. SYSTEM_BT_LPCK_DIV_FRAC_REG (0x0024)

SYSTEM_LPCLK_SEL_RTC_SLOW    Set this bit to select RTC_SLOW_CLK as the low-power clock. (R/W)

SYSTEM_LPCLK_SEL_8M    Set this bit to select RC_FAST_CLK div n clock as the low-power clock. (R/W)

SYSTEM_LPCLK_SEL_XTAL    Set this bit to select XTAL clock as the low-power clock. (R/W)

SYSTEM_LPCLK_SEL_XTAL32K    Set this bit to select xtal32k clock as the low-power clock. (R/W)

SYSTEM_LPCLK_RTC_EN    Set this bit to enable the LOW_POWER_CLK clock. (R/W)
```