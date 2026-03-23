

```markdown
| Target                     | Boundary Address                                                                 | Size (KB) | Notes |
|----------------------------|-----------------------------------------------------------------------------------|-----------|-------|
|                            | Low Address                  | High Address         |        |
| UART Controller 0          | 0x6000_0000                  | 0x6000_0FFF          | 4     |
| Reserved                   | 0x6000_1000                  | 0x6000_1FFF          |       |
| SPI Controller 1           | 0x6000_2000                  | 0x6000_2FFF          | 4     |
| SPI Controller 0           | 0x6000_3000                  | 0x6000_3FFF          | 4     |
| GPIO                       | 0x6000_4000                  | 0x6000_4FFF          | 4     |
| Reserved                   | 0x6000_5000                  | 0x6000_6FFF          |       |
| Reserved                   | 0x6000_7000                  | 0x6000_7FFF          |       |
| Low-Power Management       | 0x6000_8000                  | 0x6000_8FFF          | 4     |
| IO MUX                     | 0x6000_9000                  | 0x6000_9FFF          | 4     |
| Reserved                   | 0x6000_A000                  | 0x6000_FFFF          |       |
| UART Controller 1          | 0x6001_0000                  | 0x6001_0FFF          | 4     |
| Reserved                   | 0x6001_1000                  | 0x6001_2FFF          |       |
| I2C Controller             | 0x6001_3000                  | 0x6001_3FFF          | 4     |
| UHClO                      | 0x6001_4000                  | 0x6001_4FFF          | 4     |
| Reserved                   | 0x6001_5000                  | 0x6001_5FFF          |       |
| Remote Control Peripheral  | 0x6001_6000                  | 0x6001_6FFF          | 4     |
| Reserved                   | 0x6001_7000                  | 0x6001_8FFF          |       |
| LED PWM Controller         | 0x6001_9000                  | 0x6001_9FFF          | 4     |
| eFuse Controller           | 0x6001_A000                  | 0x6001_AFFF          | 4     |
| Reserved                   | 0x6001_B000                  | 0x6001_EFFF          |       |
| Timer Group 0              | 0x6001_F000                  | 0x6001_FFFF          | 4     |
| Timer Group 1              | 0x6002_0000                  | 0x6002_0FFF          | 4     |
| Reserved                   | 0x6002_1000                  | 0x6002_2FFF          |       |
| System Timer               | 0x6002_3000                  | 0x6002_3FFF          | 4     |
| SPI Controller 2           | 0x6002_4000                  | 0x6002_4FFF          | 4     |
| Reserved                   | 0x6002_5000                  | 0x6002_5FFF          |       |
| SYSCON                     | 0x6002_6000                  | 0x6002_6FFF          | 4     |
| Reserved                   | 0x6002_7000                  | 0x6002_AFFF          |       |
| Two-wire Automotive Interface | 0x6002_B000                | 0x6002_BFFF          | 4     |
| Reserved                   | 0x6002_C000                  | 0x6002_CFFF          |       |
| I2S Controller             | 0x6002_D000                  | 0x6002_DFFF          | 4     |
| Reserved                   | 0x6002_E000                  | 0x6003_9FFF          |       |
| AES Accelerator           | 0x6003_A000                  | 0x6003_AFFF          | 4     |
| SHA Accelerator            | 0x6003_B000                  | 0x6003_BFFF          | 4     |
| RSA Accelerator            | 0x6003_C000                  | 0x6003_CFFF          | 4     |

Cont'd on next page
```