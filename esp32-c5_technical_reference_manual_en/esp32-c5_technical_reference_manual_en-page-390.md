

```markdown
| Peripheral                     | Source Clock        | Derived Clock                                                                                   | Source Clock         | Derived Clock                          |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------|----------------------|----------------------------------------|
| XTAL_CLK                       | 48 MHz              | PLL_F240M_CLK, PLL_240 MHz                  | PLL_F160M_CLK        | 160 MHz                                |
|                                 |                     | PLL_F120M_CLK, PLL_120 MHz                  | PLL_F80M_CLK         | 80 MHz                                 |
|                                 |                     | PLL_F48M_CLK                               |                      |                                       |
| RISC-V Trace Encoder (TRACE)    |                     |                                          |                      | Y                                      |
| Interrupt priority registers    |                     |                                          |                      | Y                                      |

Table 9.2-5. Derived LP Clock Source

| Derived Clock                  | Source Clock        | Derived Clock                                                                                   | Source Clock         | Derived Clock                          |
|--------------------------------|---------------------|--------------------------------------------------------------------------------------------------|----------------------|----------------------------------------|
| XTAL_CLK                       | 48 MHz              | PLL_F480M_CLK, PLL_480 MHz                  | PLL_F240M_CLK        | 240 MHz                                |
|                                 |                     | PLL_F160M_CLK                              | PLL_F120M_CLK        | 120 MHz                                |
|                                 |                     | RC_FAST_CLK, RC_SLOW_CLK                    | OSC_SLOW_CLK         | 32 kHz                                 |
| LP_DYN_FAST_CLK                |                     |                                          |                      | Y                                      |
| LP_DYN_SLOW_CLK                |                     |                                          |                      | Y                                      |
| XTAL_D2_CLK                    |                     |                                          |                      |                                       |
| LP_FAST_CLK                    |                     |                                          |                      | Y                                      |

Table 9.2-6. LP Clocks Used by Each Peripheral

| Derived Clock                  | Source Clock        | Derived Clock                                                                                   | Source Clock         | Derived Clock                          |
|--------------------------------|---------------------|--------------------------------------------------------------------------------------------------|----------------------|----------------------------------------|
| eFuse Controller (eFuse)       | XTAL_CLK            | PLL_F480M_CLK, PLL_480 MHz                  | PLL_F240M_CLK        | 240 MHz                                |
|                                 |                     | PLL_F160M_CLK                              | PLL_F120M_CLK        | 120 MHz                                |
|                                 |                     | RC_FAST_CLK, RC_SLOW_CLK                    | OSC_SLOW_CLK         | 32 kHz                                 |
|                                 |                     |                                          |                      |                                       |
| RTC Watchdog Timer (RWD)       |                     |                                          |                      | Y                                      |
| RTC Timer (RTC Timer)          |                     |                                          |                      | Y                                      |
| Brownout Detector              |                     |                                          |                      | Y                                      |
| Power Management Unit (PMU)    |                     |                                          |                      | Y                                      |
```