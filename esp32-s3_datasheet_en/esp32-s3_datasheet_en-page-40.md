**Title: Functional Description**

---

### Feature List

- Instruction cache: 16 KB (one bank) or 32 KB (two banks)
- Data cache: 32 KB (one bank) or 64 KB (two banks)
- Instruction cache: four-way or eight-way set associative
- Data cache: four-way set associative
- Block size of 16 bytes or 32 bytes for both instruction cache and data cache
- Pre-load function
- Lock function
- Critical word first and early restart

For details, see [ESP32-S3 Technical Reference Manual > Chapter System and Memory](#).

---

### Section: eFuse Controller (4.1.2.4)

**Title:** ESP32-S3 contains a 4-Kbit eFuse to store parameters, which are burned and read by an eFuse controller.

#### Feature List

- 4 Kbits in total, with 1792 bits reserved for users, e.g., encryption key and device ID
- One-time programmable storage
- Configurable write protection
- Configurable read protection
- Various hardware encoding schemes to protect against data corruption

For details, see [ESP32-S3 Technical Reference Manual > Chapter eFuse Controller](#).

---

### Section: System Components (4.1.3)

This subsection describes the essential components that contribute to the overall functionality and control of the system.

#### Subsection 4.1.3.1 IO MUX and GPIO Matrix

**Title:** The IO MUX and GPIO Matrix in the ESP32-S3 chip provide flexible routing of peripheral input and output signals to the GPIO pins. These peripherals enhance the functionality and performance of the chip by allowing the configuration of I/O, support for multiplexing, and signal synchronization for peripheral inputs.

#### Feature List

- **GPIO Matrix:**
  - A full-switching matrix between the peripheral input/output signals and the GPIO pins
  - 175 digital peripheral input signals can be sourced from the input of any GPIO pins
  - The output of any GPIO pin is available to all other 184 digital peripheral outputs

---

**Footer:**
Espressif Systems  
[Submit Documentation Feedback](#) ESP32-S3 Series Datasheet v2.1