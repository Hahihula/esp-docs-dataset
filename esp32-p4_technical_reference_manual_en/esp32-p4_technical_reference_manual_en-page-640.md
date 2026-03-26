

```markdown
- SYS_CLK: 200 MHz
- APB_CLK: 100 MHz

Each module has an individual clock gate for the SoC clock it uses. For example, users can enable the clock for HP_CPU0 and disable the clock for HP_CPU1 by setting the `HP_SYS_CLKRST_CORE0_CPU_CLK_EN` bit and clearing the `HP_SYS_CLKRST_CORE1_CPU_CLK_EN` bit. “CPU_CLK” in bit names indicates that the corresponding clock belongs to the CPU_CLK group shown in Figure 10.2-1.

The internal PLL clocks of ESP32-P4, namely MPLL_CLK and SPLL_CLK, generate reference clocks for peripherals through a set of parallel clock dividers.

Besides these two PLL clocks, there are two additional PLL clocks dedicated to specific modules:

- SDIO_PLL, which generates three clocks:
  - SDIO_PLLO_CLK, used for SDIO’s high-speed SDIO_SLF_CLK (internal signal clock) and the source of SDIO’s low-speed clock
  - SDIO_PLL1_CLK, users for SDIO’s high-speed SDIO_DRV_CLK (output signal driving clock)
  - SDIO_PLL2_CLK, used for SDIO’s high-speed SDIO_SAM_CLK (input signal sampling clock)

- APLL_CLK, which is dedicated to I2S

A typical peripheral clock generation circuit consists of a clock selector, a clock gating unit, and a divider. In high-performance mode, the peripheral can select a high-speed clock source without division for higher processing speed. In low-power mode, the peripheral can select a low-speed clock source or divide it by a large divisor to lower power consumption. When the peripheral is disabled, its clock can be directly disabled.

Note:
Updates to `HP_SYS_CLKRST_ROOT_CLK_CTRL0/1/2/3_REG` will take effect only after `HP_SYS_CLKRST_SOC_CLK_DIV_UPDATE` is set.

10.2.4.2 LP System Clock

The LP system can operate when most other clocks are disabled. LP system clocks include LP_SLOW_CLK, LP_FAST_CLK, LP_DYN_SLOW_CLK, LP_DYN_FAST_CLK, and XTAL_D2_CLK.

The clock sources for LP_SLOW_CLK and LP_FAST_CLK are low-frequency clocks:

- LP_SLOW_CLK has four clock sources, see Table 10.2-2:

Table 10.2-2. LP_SLOW_CLK Clock Source Selection

| LP_CLKRST_SLOW_CLK_SEL | Clock Source       |
|------------------------|--------------------|
| 0                      | RC_SLOW_CLK        |
| 1                      | XTAL32K_CLK        |
| 2                      | Invalid            |
| 3                      | OSC_SLOW_CLK       |

- LP_FAST_CLK has three clock sources, see Table 10.2-3:
```