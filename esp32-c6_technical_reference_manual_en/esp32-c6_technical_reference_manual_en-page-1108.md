
```markdown
Chapter 34 SDIO Slave Controller (SDIO)

Figure 34-1. SDIO Slave Block Diagram

In the above figure, Host represents any host device that is compatible with SDIO Specification V2.00. It interacts with the ESP32-C6 (configured as the SDIO slave) via the standard SDIO bus implementation.

The SDIO Device Interface block enables effective communication with the external Host by directly providing SDIO interface registers and enabling DMA operation for high-speed data transfer over the Advanced High-Performance Bus (AHB) without engaging the CPU.

34.4 Standards Compliance

The ESP32-C6 SDIO Slave Controller conforms to the following standards:

*   SD Specifications Part1 Physical Layer Specification Version 2.00 (referred to as Physical Layer Specification V2.00 in this chapter)
*   SD Specifications Part E1 SDIO Specification Version 2.00, January 30, 2007 (referred to as SDIO Specification V2.00 in this chapter)

34.5 Functional Description

34.5.1 Physical Bus

*   Bus mode: SPI, 1-bit and 4-bit SDIO transfer modes.
*   Bus signal: The physical bus signals of the standard SDIO Specification V2.00, including CS/DI/SCLK/DO/IRQ in the SPI transmission mode, CMD/CLK/DATA/IRQ in the SDIO 1-bit transmission mode, and CMD/CLK/DAT[3:0] in the SDIO 4-bit transmission mode.
*   Bus speed mode: full-speed card mode of 0 ~ 50 MHz clock range and low-speed card mode of 0 ~ 400 kHz clock range.
*   IO functions: 2 IO functions in addition to function 0. Function 0 is only used for CCCR, FBR, and CIS operations. Function 1 and 2 can be used at the same time to transfer application data packets (such as Wi-Fi packets and Bluetooth packets) and to access SLC Host registers.

For more information, please refer to Physical Layer Specification V2.00 and SDIO Specification V2.00.
```