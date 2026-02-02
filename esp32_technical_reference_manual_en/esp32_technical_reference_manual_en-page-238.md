**Chapter Title:**
Chapter 12 DPort Registers

**Section Titles and Content:**

- **12.3.3 Interrupt Matrix Register**
  - The interrupt matrix registers are used for configuring and mapping interrupts through the interrupt matrix.
  - They are listed in Section 12.4, categorized as "Interrupt matrix registers". For a detailed description of these registers, please refer to Chapter Interrupt Matrix (INTERRUPT).

- **12.3.4 DMA Registers**
  - DMA registers are used for the SPI DMA configuration. They are listed in Section 12.4, categorized as "DMA registers".
  - For a detailed description of these registers, please refer to Chapter DMA Controller (DMA).

- **12.3.5 MPU/MMU Registers**
  - MPU/MMU registers are used for MPU/MMU configuration and operation control.
  - They are listed in Section 12.4, categorized as "MPU/MMU registers".
  - For a detailed description of these registers, please refer to Chapter Memory Management and Protection Units (MMU, MPU).

- **12.3.6 APP_CPU Controller Registers**
  - APP_CPU controller registers are used for some basic configuration of the APP_CPU.
  - Such as performing a stalling execution, and for configuring the ROM boot jump address.

- **12.3.7 Peripheral Clock Gating and Reset**
  - The following registers are used for controlling the clock gating and reset of different peripherals:
    - DPORT_PERI_CLK_EN_REG
    - DPORT_PERI_RST_EN_REG
    - DPORT_PERIP_CLK_EN_REG
    - DPORT_PERIP_RST_EN_REG
    - DPORT_WIFI_CLK_EN_REG
    - DPORT_WIFI_RST_EN_REG

  **Notice:**
  - Clock gating and reset registers are active high.
  - Reset registers cannot be cleared by hardware. Therefore, SW reset clear is required after setting the reset registers.

- ESP32 features low power consumption due to some peripheral clocks being gated (disabled) by default before using any of these peripherals it's mandatory to enable clock for given peripheral and set corresponding CLK_EN bit to 1.
  
**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:** 
ESP32 TRM (Version 5.6)
Page Number:
238