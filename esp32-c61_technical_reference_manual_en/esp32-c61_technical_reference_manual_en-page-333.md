

```markdown
| PMU_HP_x_DIG_ICG_FUNC_EN bit | control the functional clock gating of high-performance system peripherals |
|---|---|
| 0 | GDMA Controller (GDMA) |
| 1 | SPI2 |
| 2 | I2S Receive Side |
| 3 | UART0 |
| 4 | UART1 |
| 6 | USB Serial/JTAG Controller |
| 7 | I2S Transmit Side |
| 10 | MEM_MONITOR |
| 12 | Temperature Sensor |
| 13 | Timer Group 0 |
| 14 | Timer Group 1 |
| 16 | Event Task Matrix (ETM) |
| 17 | ESP-RISC-V CPU ASSIST_DEBUG |
| 18 | System Timer |
| 19 | SHA Accelerator (SHA) ECC Accelerator (ECC) Elliptic Curve Digital Signature Algorithm (ECDSA) |
| 22 | UART2 |
| 27 | LED PWM Controller (LEDC) |
| 28 | GPIO Matrix and IO MUX |
| 29 | I2C Controller (I2C) |

## 7.3 Programming Procedures

### 7.3.1 HP System Clock Configuration

When configuring `PCR_SOC_CLK_SEL` to select the clock source of `HP_ROOT_CLK`, or configuring the clock divisor for `CPU_CLK` via `PCR_CPU_DIV_NUM` and `AHB_CLK` via `PCR_AHB_DIV_NUM`, please also set the enable register `PCR_BUS_CLOCK_UPDATE` to apply the new configuration. To check whether the new configuration takes effect, read `PCR_BUS_CLOCK_UPDATE` and see if it is 0.

### 7.3.2 LP System Clock Configuration

The clock source of `LP_SLOW_CLK` can be configured via `LP_CLKRST_SLOW_CLK_SEL`. The clock source of `LP_FAST_CLK` can be configured via `LP_CLKRST_FAST_CLK_SEL`.

### 7.3.3 Peripheral Clock Reset and Configuration
```