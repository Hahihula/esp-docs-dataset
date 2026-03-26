

```markdown
| Target                                 | Boundary Address Low Address | High Address   | Size (KB) |
|----------------------------------------|------------------------------|----------------|-----------|
| LP I2C                                | 0x5012_2000                  | 0x5012_2FFF    | 4         |
| LP SPI                                | 0x5012_3000                  | 0x5012_3FFF    | 4         |
| LP Analog I2C                         | 0x5012_4000                  | 0x5012_4FFF    | 4         |
| LP I2S                                | 0x5012_5000                  | 0x5012_5FFF    | 4         |
| Reserved                              | 0x5012_6000                  | 0x5012_6FFF    | 4         |
| LP ADC                                | 0x5012_7000                  | 0x5012_7FFF    | 4         |
| Reserved                              | 0x5012_8000                  | 0x5012_9FFF    |           |
| LP GPIO Matrix                        | 0x5012_A000                  | 0x5012_AFFF    | 4         |
| LP IO MUX                             | 0x5012_B000                  | 0x5012_BFFF    | 4         |
| LP Interrupt (LP INTR)                | 0x5012_C000                  | 0x5012_CFFF    | 4         |
| LP eFuse                              | 0x5012_D000                  | 0x5012_DFFF    | 4         |
| LP Peripheral Permission (LP_PERI_PMS)| 0x5012_E000                  | 0x5012_E7FF    | 2         |
| HP2LP Peripheral Permission (HP2LP_PERI_PMS) | 0x5012_E800                  | 0x5012_EFFF    | 2         |
| LP Temperature Sensor                 | 0x5012_F000                  | 0x5012_FFFF    | 4         |

Note:
As shown in Figure 7.3-1, HP CPU and LP CPU can access HP CPU PERI, HP PERIO, HP PERI1, LP AON PERI and LP PERI listed in Table 7.3-2.
```