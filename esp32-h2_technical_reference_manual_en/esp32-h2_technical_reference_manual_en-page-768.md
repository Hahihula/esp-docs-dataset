

```markdown
- QPI mode
• Configurable module clock frequency:
    – Master: up to 48 MHz
    – Slave: up to 32 MHz
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

## 29.4 Architectural Overview

Figure 29.4-1 shows an overview of SPI module. GP-SPI2 exchanges data with SPI devices by the following ways:

• CPU-controlled transfer: CPU ↔ GP-SPI2 ↔ SPI devices
• DMA-controlled transfer: GDMA ↔ GP-SPI2 ↔ SPI devices

The signals for GP-SPI2 are prefixed with “FSPI” (Fast SPI). FSPI bus signals are routed to GPIO pins via either GPIO matrix or IO MUX. For more information, see Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX).
```

Figure 29.4-1. SPI Module Overview

```mermaid
graph TD;
    CPU -->|AHB| Bridge;
    Cache --> Bridge;
    Bridge --> APE;
    APE -->|Chan1/Chan2| GDMA;
    MSPI[MSPI] -->|SPI0/SPI1| Arbiter;
    GP-SPI2[GP-SPI2] --> Arbiter;
    Arbiter --> SPI;
    SPI --> GPIO Matrix;
    GPIO Matrix --> IO MUX;
    IO MUX --> PAD;
```

Espressif Systems 768
ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback