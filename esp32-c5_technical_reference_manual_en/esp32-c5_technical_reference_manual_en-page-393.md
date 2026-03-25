

```markdown
| PMU_HP_x_DIG_ICG_FUNC_EN bit | control the functional clock gating of high-performance system peripherals |
|------------------------------|--------------------------------------------------------------------------------|
| 0                            | GDMA Controller (GDMA)                                                          |
| 1                            | SPI2                                                                           |
| 2                            | I2S Receive Side                                                               |
| 3                            | UARTO                                                                          |
| 4                            | UART1                                                                          |
| 5                            | UHCI                                                                            |
| 6                            | USB Serial/JTAG Controller                                                     |
| 7                            | I2S Transmit Side                                                              |
| 10                           | MEM_MONITOR                                                                     |
| 11                           | SDIO Slave Controller (SDIO)                                                   |
| 12                           | Temperature Sensor                                                             |
| 13                           | Timer Group 0                                                                  |
| 14                           | Timer Group 1                                                                  |
| 16                           | Event Task Matrix (ETM)                                                         |
| 17                           | High-Performance CPU<br>ASSIST_DEBUG                                           |
| 18                           | System Timer                                                                   |
|                              | AES Accelerator (AES)<br>SHA Accelerator (SHA)<br>RSA Accelerator (RSA)<br>ECC Accelerator (ECC) |
| 19                           | Digital Signature Algorithm (DSA)<br>HMAC Accelerator (HMAC)<br>Elliptic Curve Digital Signature Algorithm (ECDSA)<br>Key Manager |
| 21                           | Remote Control Peripheral (RMT)                                                |
| 22                           | Motor Control PWM (MCPWM)                                                      |
| 24                           | BitScrambler                                                                    |
| 25                           | Parallel IO Controller (PARLIO)                                                |
| 27                           | LED PWM Controller (LEDC)                                                       |
| 28                           | GPIO Matrix and IO MUX                                                         |
| 29                           | I2C Controller (I2C)                                                            |
| 30                           | Two-wire Automotive Interface 0                                                |
| 31                           | Two-wire Automotive Interface 1                                                |

## 9.3 Programming Procedures

### 9.3.1 HP System Clock Configuration

When configuring `PCR_SOC_CLK_SEL` to select the clock source of `HP_ROOT_CLK`, or configuring the clock divisor for `CPU_CLK` via `PCR_CPU_DIV_NUM` and `AHB_CLK` via `PCR_AHB_DIV_NUM`, please also set the
```