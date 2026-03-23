

```markdown
| Target                                       | Boundary Address Low Address | High Address   | Size (KB) |
|----------------------------------------------|------------------------------|----------------|-----------|
| UART Controller 0 (UART0)                    | 0x6000_0000                  | 0x6000_OFFF    | 4         |
| UART Controller 1 (UART1)                    | 0x6000_1000                  | 0x6000_1FFF    | 4         |
| External Memory Encryption and Decryption (XTS_AES) | 0x6000_2000                  | 0x6000_2FFF    | 4         |
| Reserved                                     | 0x6000_3000                  | 0x6000_3FFF    |           |
| I2C Controller (I2C)                         | 0x6000_4000                  | 0x6000_4FFF    | 4         |
| UHCI Controller (UHCI)                       | 0x6000_5000                  | 0x6000_5FFF    | 4         |
| Remote Control Peripheral (RMT)              | 0x6000_6000                  | 0x6000_6FFF    | 4         |
| LED PWM Controller (LEDC)                    | 0x6000_7000                  | 0x6000_7FFF    | 4         |
| Timer Group 0 (TIMGO)                        | 0x6000_8000                  | 0x6000_8FFF    | 4         |
| Timer Group 1 (TIMG1)                        | 0x6000_9000                  | 0x6000_9FFF    | 4         |
| System Timer (SYSTIMER)                      | 0x6000_A000                  | 0x6000_AFFF    | 4         |
| Two-wire Automotive Interface 0 (TWAIO)      | 0x6000_B000                  | 0x6000_BFFF    | 4         |
| I2S Controller (I2S)                         | 0x6000_C000                  | 0x6000_CFFF    | 4         |
| Two-wire Automotive Interface 1 (TWAII)      | 0x6000_D000                  | 0x6000_DFFF    | 4         |
| Successive Approximation ADC (SAR_ADC)       | 0x6000_E000                  | 0x6000_EFFF    | 4         |
| USB Serial/JTAG Controller                   | 0x6000_F000                  | 0x6000_FFFF    | 4         |
| Interrupt Matrix (INTMTX)                    | 0x6001_0000                  | 0x6001_0FFF    | 4         |
| Reserved                                     | 0x6001_1000                  | 0x6001_1FFF    |           |
| Pulse Count Controller (PCNT)                | 0x6001_2000                  | 0x6001_2FFF    | 4         |
| Event Task Matrix (SOC_ETM)                  | 0x6001_3000                  | 0x6001_3FFF    | 4         |
| Motor Control PWM (MCPWM)                    | 0x6001_4000                  | 0x6001_4FFF    | 4         |
| Parallel IO Controller (PARL_IO)             | 0x6001_5000                  | 0x6001_5FFF    | 4         |
| SDIO HINF*                                   | 0x6001_6000                  | 0x6001_6FFF    | 4         |
| SDIO SLC*                                    | 0x6001_7000                  | 0x6001_7FFF    | 4         |
| SDIO SLCHOST*                                | 0x6001_8000                  | 0x6001_8FFF    | 4         |
| Reserved                                     | 0x6001_9000                  | 0x6007_FFFF    |           |
| GDMA Controller (GDMA)                       | 0x6008_0000                  | 0x6008_OFFF    | 4         |
| General Purpose SPI2 (GP-SPI2)               | 0x6008_1000                  | 0x6008_1FFF    | 4         |
| Reserved                                     | 0x6008_2000                  | 0x6008_7FFF    |           |
| AES Accelerator (AES)                        | 0x6008_8000                  | 0x6008_8FFF    | 4         |
| SHA Accelerator (SHA)                        | 0x6008_9000                  | 0x6008_9FFF    | 4         |
| RSA Accelerator (RSA)                        | 0x6008_A000                  | 0x6008_AFFF    | 4         |
| ECC Accelerator (ECC)                        | 0x6008_B000                  | 0x6008_BFFF    | 4         |
| Digital Signature (DS)                       | 0x6008_C000                  | 0x6008_CFFF    | 4         |

Cont'd on next page
```