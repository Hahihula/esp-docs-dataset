

```markdown
| PMU_HP_x_DIG_ICG_FUNC_EN Bit | Peripheral                                                                 |
|------------------------------|-----------------------------------------------------------------------------|
| 0                            | GDMA Controller (GDMA)                                                     |
| 1                            | SPI2                                                                       |
| 2                            | I2S Receive Side                                                           |
| 3                            | UARTO                                                                      |
| 4                            | UART1                                                                      |
| 5                            | UHCI                                                                        |
| 6                            | USB Serial/JTAG Controller (USB_SERIAL_JTAG)                               |
| 7                            | I2S Transmit Side                                                          |
| 10                           | Debug Assistant (ASSIST_DEBUG)                                            |
| 11                           | SDIO Slave Controller (SDIO)                                              |
| 12                           | On-Chip Sensor and Analog Signal Processing                                |
| 13                           | Timer Group 0                                                              |
| 14                           | Timer Group 1                                                              |
| 16                           | Event Task Matrix (SOC_ETM)                                                |
| 17                           | High-Performance CPU                                                       |
| 18                           | System Timer (SYSTIMER)                                                    |
| 19                           | AES Accelerator (AES)<br>SHA Accelerator (SHA)<br>RSA Accelerator (RSA)<br>ECC Accelerator (ECC)<br>Digital Signature (DS)<br>HMAC Accelerator (HMAC) |
| 21                           | Remote Control Peripheral (RMT)                                           |
| 22                           | Motor Control PWM (MCPWM)                                                 |
| 24                           | Parallel IO Transmit Side                                                  |
| 25                           | Parallel IO Receive Side                                                   |
| 27                           | LED PWM Controller (LEDC)                                                  |
| 28                           | IO MUX and GPIO Matrix (GPIO, IO MUX)                                      |
| 29                           | I2C Controller (I2C)                                                       |
| 30                           | TWAI 0                                                                      |
| 31                           | TWAI 1                                                                      |

## 8.3 Programming Procedures

### 8.3.1 HP System Clock Configuration

The clock source of HP_ROOT_CLK can be configured via `PCR_SOC_CLK_SEL`.

- If PLL_CLK is selected as the clock source of HP_ROOT_CLK,
    - the clock divisor for CPU_CLK can be configured via `PCR_CPU_HS_DIV_NUM`.
    - the clock divisor for AHB_CLK can be configured via `PCR_AHB_HS_DIV_NUM`.
```