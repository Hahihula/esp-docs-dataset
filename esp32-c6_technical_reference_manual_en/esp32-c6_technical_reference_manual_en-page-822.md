

```markdown
- QPI mode
• Configurable module clock frequency:
    – Master: up to 80 MHz
    – Slave: up to 40 MHz
• Configurable data length:
    – CPU-controlled transfer as master or as slave: 1 ~ 64 B
    – DMA-controlled single transfer as master: 1 ~ 32 KB
    – DMA-controlled configurable segmented transfer as master: data length is unlimited
    – DMA-controlled single transfer or segmented transfer as slave: data length is unlimited
• Configurable bit read/write order
• Independent interrupts for CPU-controlled transfer and DMA-controlled transfer
• Configurable clock polarity and phase
• Four SPI clock modes: mode 0 ~ mode 3
• Six CS lines as master: CS0 ~ CS5
• Able to communicate with SPI devices, such as a sensor, a screen controller, as well as a flash or RAM chip

## 28.4 Architectural Overview

Figure 28.4-1. SPI Module Overview

Figure 28.4-1 shows an overview of SPI module. GP-SPI2 exchanges data with SPI devices by the following ways:
• CPU-controlled transfer: CPU <> GP-SPI2 <> SPI devices
• DMA-controlled transfer: GDMA <> GP-SPI2 <> SPI devices

The signals for GP-SPI2 are prefixed with “FSPI” (Fast SPI). FSPI bus signals are routed to GPIO pins via either GPIO matrix or IO MUX. For more information, see Chapter 7 IO MUX and GPIO Matrix (GPIO, IO MUX).
```