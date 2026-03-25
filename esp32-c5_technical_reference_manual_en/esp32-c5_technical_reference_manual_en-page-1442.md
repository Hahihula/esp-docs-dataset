

```markdown
## 39.3 Architecture Overview

Figure 39.3-1 shows the functional block diagram of the SDIO slave module.

![Figure 39.3-1. SDIO Slave Block Diagram](image_path)

In this figure, the Host represents any device compatible with SDIO Specification V2.00. It communicates with the ESP32-C5 (configured as the SDIO slave) via the standard SDIO bus.

The SDIO Device Interface block enables efficient communication with the external host by providing direct access to SDIO interface registers. It also supports DMA operation for high-speed data transfer over the Advanced High-Performance Bus (AHB) without engaging the CPU.

## 39.4 Standards Compliance

The ESP32-C5 SDIO Slave Controller conforms to the following standards:

*   SD Specifications Part 1 Physical Layer Specification Version 2.00 (referred to as Physical Layer Specification V2.00 in this chapter)
*   SD Specifications Part E1 SDIO Specification Version 2.00, January 30, 2007 (referred to as SDIO Specification V2.00 in this chapter)

## 39.5 Functional Description

### 39.5.1 Physical Bus

*   Bus modes: SPI, 1-bit, and 4-bit SDIO transfer modes.
*   Bus signals: Standard SDIO Specification V2.00 signals, including CS/DI/SCLK/DO/IRQ for SPI mode, CMD/CLK/DATA/IRQ for SDIO 1-bit mode, and CMD/CLK/DAT[3:0] for SDIO 4-bit mode
*   Bus speed modes: Full-speed mode (0–50 MHz) and low-speed mode (0–400 kHz)
*   I/O functions: Two I/O functions in addition to function 0. Function 0 is used only for CCCR, FBR, and CIS operations. Functions 1 and 2 can be used simultaneously to transfer application data packets (such
```