

```markdown
- CPLL_CLK: internal 360 MHz PLL clock. Its reference clock is XTAL_CLK
- MPLL_CLK: internal 500 MHz PLL clock. Its reference clock is XTAL_CLK
- SPLL_CLK: internal 480 MHz PLL clock. Its reference clock is XTAL_CLK

• Slow speed clocks for LP system and some peripherals working in low-power mode
    - XTAL32K_CLK: external 32 kHz crystal clock
    - RC_SLOW_CLK: internal 150 kHz slow RC oscillator
    - OSC_SLOW_CLK: external slow clock input through XTAL_32K_N, with a frequency of 32 kHz by default. After configuring this GPIO, also configure the Hold function (see Chapter 9 GPIO Matrix and IO MUX > 9.9 Pin Hold Feature)
    - XTAL_CLK: 40 MHz external crystal clock
    - RC_FAST_CLK: internal fast RC oscillator with adjustable frequency (20 MHz by default)
    - PLL_LP_CLK: internal PLL clock with a frequency of 8 MHz by default. Its reference clock can be XTAL32K_CLK

## 10.2.4 Functional Description

### 10.2.4.1 HP System Clock

As Figure 10.2-1 shows, XTAL_CLK, CPLL_CLK, and RC_FAST_CLK are the multiplexer inputs to generate ROOT_CLK. For selecting which input, see Table 10.2-1.

**Table 10.2-1. ROOT_CLK Clock Source**

| LP_CLKRST_HP_ROOT_CLK_SRC_SEL | Clock Source |
|-------------------------------|--------------|
| 0                             | XTAL_CLK     |
| 1                             | CPLL_CLK     |
| 2                             | RC_FAST_CLK  |

ROOT_CLK is then divided by a series of dividers, and sequentially derives:

• CPU_CLK, which drives HP CPUs and their logic
• MEM_CLK, which drives the internal memories (L2 Cache, L2MEM, ROM) and their logic
• SYS_CLK, which is the HP high-speed bus clock that drives the AXI and AHB bus logic
• APB_CLK, which is the HP low-speed bus clock that drives the APB bus logic

The above four derived clocks are synchronous SoC clocks, asynchronous to peripheral clocks described in Section 10.2.4.3 Peripheral Clocks. Peripheral clocks are asynchronous with each other unless otherwise stated.

The maximum frequencies allowed for these SoC clocks are as follows. Software should ensure that the frequencies of these clocks do not exceed the maximum frequency.

• CPU_CLK: 360 MHz
• MEM_CLK: 200 MHz
```