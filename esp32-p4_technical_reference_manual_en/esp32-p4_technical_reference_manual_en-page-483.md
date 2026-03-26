

```markdown
| Target                                 | Boundary Address Low Address | High Address   | Size (KB) |
|----------------------------------------|------------------------------|----------------|-----------|
| GDMA-AXI                               |                              |                |           |
| AES Accelerator (AES)                 | 0x5008_A000                  | 0x5008_BFFF    | 8         |
| SHA Accelerator (SHA)                 | 0x5009_0000                  | 0x5009_0FFF    | 4         |
| RSA Accelerator (RSA)                 | 0x5009_1000                  | 0x5009_1FFF    | 4         |
| RSA Digital Signature Peripheral (RSA_DS)| 0x5009_2000                  | 0x5009_2FFF    | 4         |
| HMAC Accelerator (HMAC)               | 0x5009_3000                  | 0x5009_3FFF    | 4         |
| ECC Accelerator (ECC)                 | 0x5009_4000                  | 0x5009_4FFF    | 4         |
| ECDSA_DS                               | 0x5009_5000                  | 0x5009_5FFF    | 4         |
| Reserved                               | 0x5009_6000                  | 0x5009_6FFF    | 4         |
|                                        | 0x5009_7000                  | 0x5009_7FFF    |           |
| GMAC                                   | 0x5009_8000                  | 0x5009_BFFF    | 16        |
| USB 2.0 OTG High-Speed PHY             | 0x5009_C000                  | 0x5009_CFFF    | 4         |
| Reserved                               | 0x5009_D000                  | 0x5009_DFFF    |           |
| CSI Host                               | 0x5009_F000                  | 0x500F_FFFF    | 4         |
| DSI Host                               | 0x500A_0000                  | 0x500A_0FFF    | 4         |
| Image Signal Processor (ISP)           | 0x500A_1000                  | 0x500A_1FFF    | 4         |
| Remote Control Peripheral (RMT)        | 0x500A_2000                  | 0x500A_2FFF    | 4         |
| Bit-scrambler                          | 0x500A_3000                  | 0x500A_3FFF    | 4         |
| AXI ICM                                | 0x500A_4000                  | 0x500A_4FFF    | 4         |
| HP Peripheral Permission (HP_PERI_PMS) | 0x500A_5000                  | 0x5009_57FF    | 2         |
| LP2HP Peripheral Permission           | 0x500A_5800                  | 0x500A_5FFF    | 2         |
| (LP2HP_PERI_PMS)                       |                              |                |           |
| HP DMA Permission (HP_DMA_PMS)        | 0x500A_6000                  | 0x500A_6FFF    | 4         |
| H264 DMA                               | 0x500A_7000                  | 0x500A_7FFF    | 4         |
| Reserved                               | 0x500A_8000                  | 0x500B_FFFF    |           |
| HP Peripherals 1 (HP PERI1)            |                              |                |           |
| Motor Control PWMO (MCPWM0)            | 0x500C_0000                  | 0x500C_0FFF    | 4         |
| Motor Control PWM1 (MCPWM1)            | 0x500C_1000                  | 0x500C_1FFF    | 4         |
| Timer Group 0 (TIMGO)                 | 0x500C_2000                  | 0x500C_2FFF    | 4         |
| Timer Group 1 (TIMG1)                 | 0x500C_3000                  | 0x500C_3FFF    | 4         |
| I2C Controller0 (I2CO)                | 0x500C_4000                  | 0x500C_4FFF    | 4         |
| I2C Controller1 (I2C1)                | 0x500C_5000                  | 0x500C_5FFF    | 4         |
| I2S Controller0 (I2SO)                | 0x500C_6000                  | 0x500C_6FFF    | 4         |
| I2S Controller1 (I2S1)                | 0x500C_7000                  | 0x500C_7FFF    | 4         |
| I2S Controller0 (I2S2)                | 0x500C_8000                  | 0x500C_8FFF    | 4         |
| Pulse Count Controller (PCNT)          | 0x500C_9000                  | 0x500C_9FFF    | 4         |
| UART Controller 0 (UART0)              | 0x500C_A000                  | 0x500C_AFFF    | 4         |
| UART Controller 1 (UART1)              | 0x500C_B000                  | 0x500C_BFFF    | 4         |
| UART Controller 2 (UART2)              | 0x500C_C000                  | 0x500C_CFFF    | 4         |
| UART Controller 3 (UART3)              | 0x500C_D000                  | 0x500C_DFFF    | 4         |
| UART Controller 4 (UART4)              | 0x500C_E000                  | 0x500C_EFFF    | 4         |
| Parallel IO Controller (PARL_IO)       | 0x500C_F000                  | 0x500C_FFFF    | 4         |
```