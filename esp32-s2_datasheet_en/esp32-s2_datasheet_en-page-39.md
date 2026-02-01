**Title: Functional Description**

---

### **4.2 Peripherals**
This section describes the chip's peripheral capabilities, covering connectivity interfaces and on-chip sensors that extend its functionality.

#### 4.2.1 Connectivity Interface

This subsection describes the connectivity interfaces on the chip that enable communication and interaction with external devices and networks.

##### Subsection: 4.2.1.1 General Purpose Input / Output Interface (GPIO)

ESP32-S2 has 43 GPIO pins which can be assigned various functions by programming the appropriate registers. Some GPIOs can be used both for digital signals but also for analog functions, such as ADC, DAC and touch sensing.

All GPIOs can be configured as internal pull-up or pull-down, or set to high impedance, except for GPIO46, which is fixed to pull-down. When configured as an input, the input value can be read by software through the register. The input can also be set to edge-trigger or level-trigger to generate CPU interrupts. Except for GPIO46 (input only), all digital IO pins are bi-directional, non-inverting and tri-state, including input and output buffers with tristate control. These pins can be multiplexed with other functions, such as the UART, SPI, etc.

For low-power operations, the GPIOs can be set to hold their states.
For more information, please refer to [ESP32-S2 Technical Reference Manual > Chapter 10 MUX and GPIO Matrix (GPIO, IO_MUX)](#).

---

#### 4.2.1.2 SPI Controller

ESP32-S2 features four SPI interfaces (SPI0, SPI1, SPI2 and SPI3). SPI0 and SPI1 can only be configured to operate in SPI memory mode; SPI2 can be configured to operate in SPI memory and general-purpose SPI modes; SPI3 can only be configured to operate in general-purpose SPI mode.

##### Subsection: 4.2.1.2.1 SPI Memory Mode

In SPI memory mode, SPI0, SPI1 and SPI2 interface with external SPI memory. Data are transferred in unit of byte. Up to 8-line STR/DDR reads and writes are supported. The clock frequency is configurable to a maximum of 80 MHz in STR mode and a maximum of 40 MHz in DDR mode.

##### Subsection: 4.2.1.2.2 SPI2 General-purpose SPI (GP-SPI) mode

When SPI2 acts as a general-purpose SPI, it can operate in master and slave modes. The master mode supports 2-line full-duplex communication and 1-2-/4-/8-line half-duplex communication. The slave mode supports 2-line full-duplex communication and 1-2-/4-/8-line half-duplex communication. The host’s clock frequency is configurable. Data are transferred in unit of byte. The clock polarity (CPOL) and phase (CPHA) are also configurable. The SPI2 interface supports DMA.

- In 2-line full-duplex communication mode, the host's clock frequency is configurable to 80 MHz at most, and the slave’s clock frequency to 40 MHz at most. Four modes of SPI transfer format are supported.
- In 1-/2-/4-/8-line half-duplex communication mode, the host’s clock frequency is configurable to 80 MHz at most and the four modes of SPI transfer format are supported.

---

**Footer:**
Espressif Systems
39 Submit Documentation Feedback ESP32-S2 Series Datasheet v1.8