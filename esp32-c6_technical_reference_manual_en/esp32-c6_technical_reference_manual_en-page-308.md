

```markdown
- High-speed clock sources for devices working at a higher frequency, such as CPU and digital peripherals
    - PLL_CLK (480 MHz): internal PLL clock. Its reference clock is XTAL_CLK.
    - XTAL_CLK (40 MHz): external crystal clock
- Slow-speed clock sources for LP system and some peripherals working in low-power mode
    - XTAL32K_CLK (32 kHz): external crystal clock
    - RC_FAST_CLK (17.5 MHz by default): internal fast RC oscillator with adjustable frequency
    - RC_SLOW_CLK (136 kHz by default): internal slow RC oscillator
    - OSC_SLOW_CLK (32 kHz by default): external slow clock input through XTAL_32K_P. After configuring this GPIO, also configure the Hold function (see Chapter 7 IO MUX and GPIO Matrix (GPIO, IO MUX) > 7.9 Pin Hold Feature)
```

## 8.2.4 Functional Description

### 8.2.4.1 HP System Clock

As Figure 8.2-1 shows, CPU_CLK is the master clock for CPU and it can be as high as 160 MHz when CPU works in high performance mode. Alternatively, CPU can run at lower frequencies, such as at 2 MHz, to achieve lower power consumption. CPU_CLK shares the same clock sources with AHB_CLK, CRYPTO_CLK, and MSPI_CLK. Users can select from XTAL_CLK, PLL_CLK, or RC_FAST_CLK as the clock source of CPU_CLK by configuring `PCR_SOC_CLK_SEL`. See Table 8.2-1 and Table 8.2-2. When PLL_CLK is selected as the clock source, CPU_CLK will be divided into 160 MHz clock by hardware control before the configurable divider, please refer to AUTODIV in figure 8.2-1. By default, the CPU clock is sourced from XTAL_CLK with a divider of 1, i.e., the CPU clock is 40 MHz.

Table 8.2-1. CPU_CLK Clock Source

| PCR_SOC_CLK_SEL | CPU Clock Source |
|------------------|------------------|
| 0                | XTAL_CLK         |
| 1                | PLL_CLK          |
| 2                | RC_FAST_CLK      |
```