

```markdown
- High-performance (HP) clocks for devices working at a higher frequency, such as CPU and digital peripherals

    - PLL_F96M_CLK (96 MHz): internal PLL clock. Its reference clock is XTAL_CLK.
    - PLL_F64M_CLK (64 MHz): internal PLL clock. Its reference clock is XTAL_CLK.
    - XTAL_CLK (32 MHz): external crystal clock
- Low-power (LP) clocks for low-power system and some peripherals working in low-power mode

    - XTAL32K_CLK (32 kHz): external crystal clock
    - RC_FAST_CLK (8 MHz by default): internal fast RC oscillator with adjustable frequency
    - RC_SLOW_CLK (130 kHz): internal slow RC oscillator
    - OSC_SLOW_CLK (32 kHz by default): external slow clock input through XTAL_32K_P. After configuring this GPIO, also configure the Hold function (see Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX) > 6.9 Pin Hold Feature)
    - PLL_LP_CLK (8 MHz): internal PLL clock, with reference clock XTAL32K_CLK
```

## 7.2.4 Functional Description

### 7.2.4.1 HP System Clock

As Figure 7.2-1 shows, CPU_CLK is the master clock for CPU and its frequency can be as high as 96 MHz. Alternatively, CPU can run at lower frequencies, such as at 2 MHz, to achieve lower power consumption. CPU_CLK shares the same clock sources with AHB_CLK and APB_CLK. Users can select from XTAL_CLK, PLL_96M_CLK, PLL_64M_CLK, or RC_FAST_CLK as the clock source of CPU_CLK by configuring `PCR_SOC_CLK_SEL`. For details, see Table 7.2-1 and Table 7.2-2. By default, the CPU clock is sourced from XTAL_CLK with a divider of 1, i.e., the CPU clock frequency is 32 MHz.

Table 7.2-1. CPU_CLK Clock Source

| PCR_SOC_CLK_SEL | CPU Clock Source |
|------------------|------------------|
| 0                | XTAL_CLK         |
| 1                | PLL_F96M_CLK     |
| 2                | RC_FAST_CLK      |
| 3                | PLL_F64M_CLK     |
```