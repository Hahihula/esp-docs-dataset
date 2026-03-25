
```markdown
| Target | Boundary Address Low Address | High Address | Size (KB) |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------|:--------------|:-----------|
| UART Controller 0 (UART0) | 0x6000_0000 | 0x6000_0FFF | 4 |
| UART Controller 1 (UART1) | 0x6000_1000 | 0x6000_1FFF |   |
| External Memory Encryption and Decryption (XTS_AES)¹ | 0x6000_2000 | 0x6000_2FFF |   |
| SPI Controller 0 (SPI0)¹ | 0x6000_2000 | 0x6000_2FFF |   |
| SPI Controller 1 (SPI1) | 0x6000_3000 | 0x6000_3FFF |   |
| I2C Controller (I2C) | 0x6000_4000 | 0x6000_4FFF |   |
| Reserved | 0x6000_5000 | 0x6000_5FFF |   |
| UART Controller 2 (UART2) | 0x6000_6000 | 0x6000_6FFF |   |
| LED PWM Controller (LEDC) | 0x6000_7000 | 0x6000_7FFF |   |
| Timer Group 0 (TIMGO) | 0x6000_8000 | 0x6000_8FFF |   |
| Timer Group 1 (TIMG1) | 0x6000_9000 | 0x6000_9FFF |   |
| System Timer (SYSTIMER) | 0x6000_A000 | 0x6000_AFFF |   |
| Reserved | 0x6000_B000 | 0x6000_BFFF |   |
| I2S Controller (I2S) | 0x6000_C000 | 0x6000_CFFF |   |
| Reserved | 0x6000_D000 | 0x6000_DFFF |   |
| SAR ADC | 0x6000_E000 | 0x6000_EFFF |   |
| USB Serial/JTAG Controller (USB_SERIAL_JTAG) | 0x6000_F000 | 0x6000_FFFF |   |
| Interrupt Matrix | 0x6001_0000 | 0x6001_0FFF |   |
| Reserved | 0x6001_1000 | 0x6001_2FFF |   |
| Event Task Matrix (SOC_ETM) | 0x6001_3000 | 0x6001_3FFF |   |
| Reserved | 0x6001_4000 | 0x6001_9FFF |   |
| Memory Access Monitor (PSARM_MEM_MONITOR)² | 2 | 0x6001_A000 | 0x6001_AFFF | 4 |
| Reserved | | 0x6001_B000 | 0x6007_FFFF |   |
| General DMA Controller (GDMA) | 0x6008_0000 | 0x6008_0FFF |   |
| General Purpose SPI2 Controller (GP-SPI2) | 0x6008_1000 | 0x6008_1FFF |   |
| Reserved | 0x6008_2000 | 0x6008_8FFF |   |
| SHA Accelerator (SHA) | 0x6008_9000 | 0x6008_9FFF |   |
| Reserved | 0x6008_A000 | 0x6008_AFFF |   |
| ECC Accelerator (ECC) | 0x6008_B000 | 0x6008_BFFF |   |
| Reserved | 0x6008_C000 | 0x6008_DFFF |   |
| ECDSA Accelerator (ECDSA) | 0x6008_E000 | 0x6008_EFFF |   |
| Reserved | 0x6008_F000 | 0x6008_FFFF |   |
| IO MUX | 0x6009_0000 | 0x6009_0FFF |   |
| GPIO Matrix | 0x6009_1000 | 0x6009_1FFF |   |
| Memory Access Monitor (TCM_MEM_MONITOR)² | 1 | 0x6009_2000 | 0x6009_2FFF |   |
| Power Always-on Unit (PAU) | | 0x6009_3000 | 0x6009_3FFF |   |

Cont'd on next page
```