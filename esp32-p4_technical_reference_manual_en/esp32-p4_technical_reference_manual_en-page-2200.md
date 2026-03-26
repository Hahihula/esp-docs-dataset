

# 43.4 Architectural Overview

Figure 43.4-1. SPI Module Overview

* SPI0 includes FLASH MSPI SPI0 and PSRAM MSPI SPI0.
* SPI1 includes FLASH MSPI SPI1 and FLASH MSPI SPI1.

Figure 43.4-1 shows an overview of this SPI module. GP-SPI2, GP-SPI3, and LP-SPI exchange data with SPI devices by the following ways:

- CPU-controlled transfer:
    - CPU ↔ LP-SPI ↔ SPI devices
    - CPU ↔ GP-SPI2 (GP-SPI3) ↔ SPI devices

- DMA-controlled transfer: DMA ↔ GP-SPI2 (GP-SPI3) ↔ SPI devices

In this chip, “SPI2”, “SPI3”, and “LP_SPI” are used as prefixes of GP-SPI2, GP-SPI3, and LP-SPI input and output signal buses to illustrate the SPI bus functions.

SPI2 bus signals are routed to GPIO pins via either the HP GPIO matrix or the HP IO MUX, while SPI3 bus signals are routed to GPIO pins via the HP GPIO matrix only. LP_SPI bus signals are routed via the LP GPIO matrix only. For more information, see Chapter 9 GPIO Matrix and IO MUX.

The functionalities of GP-SPI3 are nearly the same as those of GP-SPI2. The functionalities of LP-SPI are a subset of the GP-SPI functionalities. GP-SPI2’s functionalities are described in Section 43.5. The differences among GP-SPI2, GP-SPI3, and LP-SPI are described in Section 43.5.1 and Section 43.10.