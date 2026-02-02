**Title: Chapter 20 SPI Controller (SPI)**

---

### 20.1 Overview

As Figure **20.1-1. SPI Architecture** shows, ESP32 integrates four SPI controllers which can be used to communicate with external devices that use the SPI protocol. Controller SPIO is used as a buffer for accessing external memory.

Controller SPI1 can be used as a master. Controllers SPI2 and SPI3 can be configured as either a master or a slave. When used as a master, each SPI controller can drive multiple CS signals (CS0~CS2) to activate multiple slaves. Controllers SPI1-SPI3 share two DMA channels.

The SPI signal buses consist of D, Q, QO-CS2, CLK, WP, and HD signals, as Table **20.1-1** shows. Controllers SPIO and SPI1 share one signal bus through an arbiter; the signals of the shared bus start with “SPI”. Controllers SPI2 and SPI3 use signal buses starting with “HSPI” and “VSPI” respectively.

The I/O lines included in the above-mentioned signal busses can be mapped to pins via either the IO_MUX module or the GPIO matrix. (Please refer to Chapter **IO_MUX** for details.)

The SPI controller supports four-line full-duplex/half-duplex communication (MOSI, MISO, CS, and CLK lines) and three-line half-duplex-only communication (DATA, CS, and CLK lines) in GP-SPI mode. In QSPI mode, an SPI controller accesses the flash or SRAM by using signal buses D, Q, CSO-CS2, CLK, WP, and HD as a four-bit parallel SPI bus.

The mapping between SPI bus signals and pin function signals under different communication modes is shown in Table **20.1-1**.

---

**Table 20.1-1: Mapping Between SPI Bus Signals and Pin Function Signals**

| Four-line GP-SPI | Three-line GP-SPI | QSPI Signal |
|------------------|--------------------|-------------|
| Full-duplex/half-duplex signal bus MOSI | Half-duplex signal bus D, Q, CSO-CS2, CLK, WP, HD as a four-bit parallel SPI bus | Pin function signals |
| MOSI DATA        |                    | HSPID       |
| MISO            |                    | VSPIQ       |

---

**Footer:**
Espressif Systems  
354 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback