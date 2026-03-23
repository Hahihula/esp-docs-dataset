

```markdown
| Component | Clock Enabling Bit¹ | Reset Controlling Bit²³ |
|-----------|---------------------|--------------------------|
| 1 Set the clock enable bit to 1 to enable the clock, and to 0 to disable the clock; <br>2 Set the reset enabling bit to 1 to reset a peripheral, and to 0 to disable the reset. <br>3 Reset registers cannot be cleared by hardware. Therefore, SW reset clear is required after setting the reset registers. <br>4 UART memory is shared by all UART peripherals, meaning having any active UART peripherals will prevent the UART memory from entering the clock-gated state. <br>5 When DMA is required for peripheral communications, for example, UCHIO, SPI2, I2S, AES, SHA, and ADC, DMA clock should also be enabled. <br>6 Resetting this bit also resets the SHA accelerator. <br>7 Resetting this bit also resets the AES, SHA, and RSA accelerators. |
```