**Title: Functional Description**

---

### **4.1.3 System Components**

This subsection describes the essential components that contribute to the overall functionality and control of the system.

#### **4.1.3.1 IO MUX and GPIO Matrix**

The IO MUX and GPIO Matrix in the ESP32-H2 chip provide flexible routing of peripheral input and output signals to the GPIO pins. These peripherals enhance the functionality and performance of the chip by allowing the configuration of I/O, support for multiplexing, and signal synchronization for peripheral inputs.

**Feature List**
- 19 GPIO pins for general-purpose I/O or connection to internal peripheral signals
- **GPIO matrix:**
  - Routing 78 peripheral input and 99 output signals to any GPIO pin
  - Signal synchronization for peripheral inputs based on IO MUX operating clock
  - GPIO Filter hardware for input signal filtering
  - Glitch Filter hardware for second time filtering on input signal
  - Sigma delta modulated (SDM) output
  - GPIO simple input and output

- IO MUX for directly connecting certain digital signals (SPI, JTAG, UART) to pins
- Support for Event Task Matrix

For details, see ESP32-H2 Technical Reference Manual > Chapter 10 MUX and GPIO Matrix.

---

### **4.1.3.2 Reset**

The ESP32-H2 chip provides four types of reset that occur at different levels, namely CPU Reset, Core Reset, System Reset, and Chip Reset. Except for Chip Reset, all reset types preserve the data stored in internal memory.

**Feature List**
- Four types of reset:
  - CPU Reset – Resets the CPU core
  - Core Reset – Resets the whole digital system except for the LP system
  - System reset – Resets the whole digital system, including the LP system
  - Chip reset – Resets the whole chip

- **Reset trigger:**
  - Directly by hardware
  - Via software by configuring the corresponding registers of the CPU

---

**Footer:**  
Espressif Systems  
30  
Submit Documentation Feedback  
ESP32-H2 Series Datasheet v1.2