

```markdown
- DMA-controlled configurable segmented transfer as master: data length is unlimited
- DMA-controlled single transfer or segmented transfer as slave: data length is unlimited
• Configurable bit read/write order
• Independent interrupts for CPU-controlled transfer and DMA-controlled transfer
• Configurable clock polarity and phase
• Four SPI clock modes: mode 0~mode 3
• Multiple CS lines as master

    - GP-SPI2: CSO~CS5
    - GP-SPI3: CSO~CS2

• Able to communicate with SPI devices, such as a sensor, a screen controller, as well as a flash or RAM chip

LP-SPI is a simplified version of GP-SPI and has a subset of GP-SPI's features:

• Works as a master or as a slave
• Half- and full-duplex communications
• CPU-controlled transfer
• 1-bit SPI data mode
• Configurable module clock frequency:
    - Master: up to 40 MHz
    - Slave: up to 40 MHz
• Configurable data length:
    - CPU-controlled transfer as master or as slave: 1~64 bytes
• Configurable bit read/write order
• Interrupts for CPU-controlled transfer
• Configurable clock polarity and phase
• Four SPI clock modes: mode 0~mode 3
• One CS line as master: CSO
• Wake-up feature as slave (the only new feature compared with GP-SPI)
```