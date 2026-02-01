**Title: Functional Description**

---

### **4.1.3.1 IO MUX and GPIO Matrix**

The IO MUX and GPIO Matrix in the ESP32-C61 chip provide flexible routing of peripheral input and output signals to the GPIO pins. These peripherals enhance the functionality and performance of the chip by allowing the configuration of I/O, support for multiplexing, and signal synchronization for peripheral inputs.

**Feature List**
- 30 GPIO pins for general-purpose I/O or connection to internal peripheral signals
- GPIO matrix:
  - Routing 37 peripheral input and 57 output signals to any GPIO pin
  - Signal synchronization for peripheral inputs based on IO MUX operating clock
  - GPIO Filter hardware for input signal filtering
  - IO MUX for directly connecting certain digital signals (SPI, JTAG, UART, SPIO) to pins
  - Support for Event Task Matrix

---

### **4.1.3.2 Reset**

The ESP32-C61 chip provides four types of reset that occur at different levels, namely CPU Reset, Core Reset, System Reset, and Chip Reset. Except for Chip Reset, all reset types preserve the data stored in internal memory.

**Feature List**
- Four types of reset:
  - CPU Reset – Resets the CPU core
  - Core Reset – Resets the whole digital system except for the LP system
  - System Reset – Resets the whole digital system, including the LP system
  - Chip Reset – Resets the whole chip

**Reset trigger:**
- Directly by hardware
- Via software by configuring the corresponding registers of the CPU
- Support for retrieving reset cause

---

### **4.1.3.3 Clock**

The ESP32-C61 chip has clocks sourced from oscillators, RC circuits, and PLL circuits, which are then processed by dividers or selectors. The clocks can be classified into high-speed clocks for devices working at higher frequencies and slow-speed clocks for low-power systems and some peripherals.

---

**Footer:**
Espressif Systems
35 ESP32-C61 Series Datasheet v0.5