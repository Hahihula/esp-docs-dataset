**Title: Functional Description**

- one-time programmable storage
- configurable write protection
- configurable read protection
- various hardware encoding schemes to protect against data corruption

For details, see [ESP32-C5 Technical Reference Manual > Chapter eFuse Controller](#).

---

**Subtitle: 4.1.2.4 cache**

ESP32-C5 has an four-way set associative cache.

**Feature List**
- size: 32 KB
- block size: 32 bytes
- pre-load function
- lock function
- critical word first and early restart

For details, see [ESP32-C5 Technical Reference Manual > Chapter Cache](#).

---

**Title: System Components**

This subsection describes the essential components that contribute to the overall functionality and control of the system.

**Subtitle: 4.1.3 IO MUX and GPIO Matrix**

The IO MUX and GPIO Matrix in the ESP32-C5 chip provide flexible routing of peripheral input and output signals to the GPIO pins. These peripherals enhance the functionality and performance of the chip by allowing the configuration of I/O, support for multiplexing, and signal synchronization for peripheral inputs.

**Feature List**
- 29 GPIO pins for general-purpose I/O or connection to internal peripheral signals
- GPIO matrix:
  - routing 77 peripheral input and 75 output signals to any GPIO pin
  - signal synchronization for peripheral inputs based on IO MUX operating clock
  - GPIO Filter hardware for input signal filtering

- IO MUX for directly connecting certain digital signals (SPI, JTAG, UART) to pins
- support for Event Task Matrix

For details, see [ESP32-C5 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](#).

---

**Footer:**
Espressif Systems  
[Submit Documentation Feedback](#)  
Page 38 ESP32-C5 Series Datasheet v1.0