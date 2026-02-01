**Title: Functional Description**

---

### SPI3 General-purpose SPI (GP-SPI) mode

As a general-purpose SPI interface, SPI3 can operate in master and slave modes. In 2-line full-duplex and 1-line half-duplex communication modes.

- **In 2-line full-duplex communication mode**, the host's clock frequency is configurable to a maximum of 80 MHz, and the slave’s clock frequency to 40 MHz at most.
  
- **In 1-line half-duplex communication mode**, the host’s clock frequency is configurable to a maximum of 80 MHz, and the slave’s clock frequency to 40 MHz at most.

The four modes of SPI transfer format are supported in both cases. The mapping between SPI bus signals and GPIO pins can be found [Table 4-1 Mapping of SPI Signal Buses and Chip Pins](#).

---

**Table: Table 4-1. Mapping of SPI Signal Buses and Chip Pins**

| Standard SPI | Extended SPI |
|--------------|--------------|
| Full-Duplex  | Half-Duplex  | Pin Functions | SPI3 Signal Bus |
| SPI Signal Bus | SPI Signal Bus | SPI3 Signal Bus |
| MOSI         | MOSI         | D             | FSPID          | SPI3_D       |
| MISO (MISO)   | Q            | SPIDQ         | FSPIQ          | SPI3_Q       |
| CS           | CS           | SPICS0 ~ 1    | FSPICSO ~ 5   | SPI3_CS0 ~ 2 |
| CLK          | CLK          | SPICLK        | FSPICLK        | SPI3_CLK     |

In most cases, the data port connection between ESP32-S2 and external flash is as follows:

- **SPI8-line mode:**
  - SPID (SPIID) = IO0
  - SPIQ (SPIQ) = IO1
  - SPIWP (SPIWP) = IO2
  - SPIHPD (SPIHD) = IO3
  - GPIO33 = IO4
  - GPIO34 = IO5

---

**Footer:**
Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32-S2 Series Datasheet v1.8