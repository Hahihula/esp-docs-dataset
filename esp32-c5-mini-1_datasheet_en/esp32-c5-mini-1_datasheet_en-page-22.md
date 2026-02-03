**Title: Peripherals**

---

### Pin Assignment

The pins for the USB Serial/JTAG controller are multiplexed with GPIO13 ~ GPIO14 via IO MUX. GPIO13 ~ GPIO14 are also multiplexed with the pins for the SDIO Slave controller. The SDIO Slave controller can be used together with the USB Serial/JTAG controller in single SPI mode, but not in quad SPI mode.

For more information about the pin assignment, see [ESP32-C5 Series Datasheet](#) > Section IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

### 5.2.1.6 CAN FD Controller

The Controller Area Network Flexible Data-Rate (CAN FD) is a multi-master, multi-cast communication protocol designed for automotive applications. The CAN FD controller facilitates the communication based on this protocol.

#### Feature List
- compliant with ISO11898-1:2015
- RX buffer FIFO with 32 - 4096 words (1 - 204 CAN FD frames with 64 byte of data)
- 2 - 8 TXT buffers (1 CAN FD frame in each TXT buffer)
- 32-bit slave memory interface (APB, AHB, RAM-like interface)
- support of ISO and non-ISO CAN FD protocol
- timestamping and time triggered transmission
- support interrupts
- loopback mode, bus monitoring mode, ACK forbidden mode, self-test mode, and restricted operation mode

For details, see ESP32-C5 Technical Reference Manual > Chapter Controller Area Network Flexible Data-Rate.

---

### Pin Assignment (Repeated)

The pins for the CAN FD Controller can be chosen from any GPIOs via the GPIO Matrix. For more information about the pin assignment, see [ESP32-C5 Series Datasheet](#) > Section IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

### 5.2.1.7 LED PWM Controller

The LED PWM controller can generate independent digital waveform on six channels.

#### Feature List
- generating digital waveform with configurable periods and duty cycle. The resolution of duty cycle can be up to 20 bits
- multiple clock sources, including 80 MHz PLL clock, external main crystal clock, and internal fast RC oscillator

---

**Footer:**
Espressif Systems  
Page number: 22  
Submit Documentation Feedback  

ESP32-C5-MINI-1 Datasheet v1.0