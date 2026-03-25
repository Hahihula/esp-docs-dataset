

```markdown
| Target | Boundary Address Low Address | High Address | Size (KB) |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------|:--------------|:-----------|
| UART Controller 0 (UART0) | 0x6000_0000 | 0x6000_OFFF | 4 |
| UART Controller 1 (UART1) | 0x6000_1000 | 0x6000_1FFF | 4 |
| External Memory Encryption and Decryption (XTS_AES)¹ | 0x6000_2000 | 0x6000_2FFF | 4 |
| SPI Controller 0 (SPI0)³ | 0x6000_2000 | 0x6000_2FFF | 4 |
| SPI Controller 1 (SPI1) | 0x6000_3000 | 0x6000_3FFF | 4 |
| I2C Controller (I2C) | 0x6000_4000 | 0x6000_4FFF | 4 |
| UHCI Controller (UHCI) | 0x6000_5000 | 0x6000_5FFF | 4 |
| Remote Control Peripheral (RMT) | 0x6000_6000 | 0x6000_6FFF | 4 |
| LED PWM Controller (LEDC) | 0x6000_7000 | 0x6000_7FFF | 4 |
| Timer Group 0 (TIMGO) | 0x6000_8000 | 0x6000_8FFF | 4 |
| Timer Group 1 (TIMG1) | 0x6000_9000 | 0x6000_9FFF | 4 |
| System Timer (SYSTIMER) | 0x6000_A000 | 0x6000_AFFF | 4 |
| Two-wire Automotive Interface 0 (TWAIO) | 0x6000_B000 | 0x6000_BFFF | 4 |
| I2S Controller (I2S) | 0x6000_C000 | 0x6000_CFFF | 4 |
| Two-Wire Automotive Interface 1 (TWAI1) | 0x6000_D000 | 0x6000_DFFF | 4 |
| SAR ADC | 0x6000_E000 | 0x6000_EFFF | 4 |
| Temperature Sensor | 0x6000_E000 | 0x6000_EFFF | 4 |
| USB Serial/JTAG Controller (USB_SERIAL_JTAG) | 0x6000_F000 | 0x6000_FFFF | 4 |
| Interrupt Matrix (INTMTX) | 0x6001_0000 | 0x6001_OFFF | 4 |
| Reserved | 0x6001_1000 | 0x6001_1FFF |   |
| Pulse Count Controller (PCNT) | 0x6001_2000 | 0x6001_2FFF | 4 |
| Event Task Matrix (SOC_ETM) | 0x6001_3000 | 0x6001_3FFF | 4 |
| Motor Controller (MCPWM) | 0x6001_4000 | 0x6001_4FFF | 4 |
| Parallel IO Controller (PARL_IO) | 0x6001_5000 | 0x6001_5FFF | 4 |
| SDIO HINF² | 0x6001_6000 | 0x6001_6FFF | 4 |
| SDIO SLC² | 0x6001_7000 | 0x6001_7FFF | 4 |
| SDIO SLCHOST² | 0x6001_8000 | 0x6001_8FFF | 4 |
| Reserved | 0x6001_6000 | 0x6001_9FFF |   |

Cont’d on next page
```