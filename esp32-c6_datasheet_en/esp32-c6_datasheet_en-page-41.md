**4 Functional Description**

---

### Feature List

- Configure write protection for some blocks
- Configure read protection for some blocks
- Various hardware encoding schemes against data corruption

For details, see [ESP32-C6 Technical Reference Manual > Chapter eFuse Controller](#).

---

#### 4.1.3 System Components

This subsection describes the essential components that contribute to the overall functionality and control of the system.

---

##### 4.1.3.1 IO MUX and GPIO Matrix

The IO MUX and GPIO Matrix in the ESP32-C6 chip provide flexible routing of peripheral input and output signals to the GPIO pins. These peripherals enhance the functionality and performance of the chip by allowing the configuration of I/O, support for multiplexing, and signal synchronization for peripheral inputs.

**Feature List**

- 30 or 22 GPIO pins for general-purpose I/O or connection to internal peripheral signals
- GPIO matrix:
  - Routing 85 peripheral input and 93 output signals to any GPIO pin
  - Signal synchronization for peripheral inputs based on IO MUX operating clock
  - GPIO Filter hardware for input signal filtering
  - Glitch Filter hardware for second time filtering on input signal
  - Sigma delta modulated (SDM) output

- IO MUX for directly connecting certain digital signals (SPI, JTAG, UART) to pins
- LP IO MUX for controlling edge LP GPIO pins (GPIO0 ~ GPIO7) used by peripherals in the LP system
- Support for Event Task Matrix

For details, see [ESP32-C6 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](#).

---

#### 4.1.3.2 Reset

The ESP32-C6 chip provides four types of reset that occur at different levels, namely CPU Reset, Core Reset, System Reset, and Chip Reset. Except for Chip Reset, all reset types preserve the data stored in internal memory.

**Feature List**

- Four types of reset:
  - CPU Reset – Resets the CPU core

Espressif Systems  
41  
[ESP32-C6 Series Datasheet v1.4](#)  
Submit Documentation Feedback