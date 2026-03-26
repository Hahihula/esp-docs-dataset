

```markdown
| Derived clock | RC_SLOW_CLK 150 kHz | XTAL32K_CLK 32 kHz | OSC_SLOW_CLK 32 MHz | RC_FAST_CLK 20 MHz | XTAL_PLL_LP_CLK 40 MHz | 8 MHz | LP_SLOW_CLK | LP_FAST_CLK | LP_DYN_SLOW_CLK | LP_DYN_FAST_CLK | LP_PERI_CLK | XTAL_D2_CLK | Clock from IO |
|---------------|--------------------:|-------------------:|---------------------:|---------------------:|------------------------:|-------:|------------:|------------:|-----------------:|-----------------:|-------------:|--------------:|---------------|
| eFuse Controller (EFUSE) |                 |                   |                     |                     |                        |       |            |            |                 |                 |             |              |               |
| RTC Watchdog Timer (RWDT) |        Y |                   |                     |                     |                        |       |            |            |                 |                 |             |              |               |
| RTC Timer |           |                   |                     |                     |                        |       |            |            |                 |                 |             |              |               |
| Brown-out Detector |          |                   |                     |                     |                        |       |            |            |                 |                 |             |              |               |
| Power Management Unit (PMU) |         |                   |                     |                     |                        |       |            |      Y      |                 |                 |             |              |               |
| LP UART |          |                   |                     |                     |                        |       |     Y       |            |                 |                 |             |              | PAD_LP_UART_SL_P_CLK |
| LP SPI |         |                   |                     |                     |                        |       |            |            |                 |                 |             |              | PAD_LP_SPI_CLK |
| LP I2C |          |                   |                     |                     |                        |       |            |            |                 |                 |             |              |               |
| Analog I2C Controller |         |                   |                     |                     |                        |       |            |            |                 |                 |             |              |               |
| LP I2S Controller |          |                   |                     |                     |                        |       |     Y       |            |                 |                 |             |              |               |
| LP ADC Controller |         |                   |                     |                     |                        |       |            |            |                 |                 |      Y       |              |               |
```