**Title: Functional Description**

---

### **4.8 Digital Peripherals**

#### **4.8.1 General Purpose Input / Output Interface (GPIO)**

ESP32 has 34 GPIO pins which can be assigned various functions by programming the appropriate registers. There are several kinds of GPIOs: digital-only, analog-enabled, capacitive-touch-enabled, etc. Analog-enabled GPIOs and Capacitive-touch-enabled GPIOs can be configured as digital GPIOs.

Most of the digital GPIOs can be configured as internal pull-up or pull-down, or set to high impedance. When configured as an input, the input value can be read through the register. The input can also be set to edge-trigger or level-trigger to generate CPU interrupts. Most of the digital IO pins are bi-directional, non-inverting and tristate, including input and output buffers with tristate control. These pins can be multiplexed with other functions, such as the SDIO, UART, SPI, etc. (More details can be found in the Appendix, Table IO_MUX). For low-power operations, the GPIOs can be set to hold their states.

For details, see Section 4.10 Peripheral Pin Configurations, Appendix A –ESP32 Pin Lists and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

#### **4.8.2 Serial Peripheral Interface (SPI)**

ESP32 integrates four SPI controllers which can be used to communicate with external devices that use the SPI protocol. Controller SPI0 is used as a buffer for accessing external memory. Controller SPI1 can be used as a master. Controllers SPI2 and SPI3 can be configured as either a master or a slave.

SPI1, SPI2, and SPI3 use signal buses prefixed with SPI, HSPI, and VSPI, respectively.

##### Features of General Purpose SPI (GP-SPI)

- Programmable data transfer length, in multiples of 1 byte
- Four-line full-duplex/half-duplex communication and three-line half-duplex communication support
- Master mode and slave mode
- Programmable CPOL and CPHA
- Programmable clock

For details, see ESP32 Technical Reference Manual > Chapter SPI Controller.

##### Pin Assignment

For SPI, the pins are multiplexed with GPIO6 ~ GPIO11 via the IO MUX. For HSPI, the pins are multiplexed with GPIO2, GPIO4, GPIO12 ~ GPIO15 via the IO MUX. For VSPI, the pins are multiplexed with GPIO5, GPIO18 ~ GPIO19, GPIO21 ~ GPIO23 via the IO MUX.

For more information about the pin assignment, see Section 4.10 Peripheral Pin Configurations and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

---

### **4.8.3 Universal Asynchronous Receiver Transmitter (UART)**

The UART in the ESP32 chip facilitates the transmission and reception of asynchronous serial data between the chip and external UART devices. It consists of two UARTs in the main system, and one low-power LP UART.

Espressif Systems  
ESP32 Series Datasheet v5.2  

[Submit Documentation Feedback](#)