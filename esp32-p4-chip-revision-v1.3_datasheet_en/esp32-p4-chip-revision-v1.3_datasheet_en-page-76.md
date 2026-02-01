**Title: Functional Description**

---

### **4.2.2.19 BitScrambler**

The ESP32-P4 has an extensive amount of DMA-capable peripherals. These can move data from memory to external device, and vice versa, without any interference from the CPU. This only works if the external device needs or emits the data in question in the same format as the software expects it: if not, the CPU needs to rewrite the format of the data. Examples include a need to swap bytes, reverse bytes, and shift the data left or right.

Since bitwise operations can be relatively CPU-intensive and DMA is designed specifically to offload such work from the CPU, ESP32-P4 integrates two dedicated peripherals called BitScramblers. These modules are designed to transform data formats during transfers between memory and peripherals. One BitScrambler handles memory-to-peripheral (or memory-to-memory) transfers, while the other is dedicated to peripheral-to-memory transfers. While BitScramblers can handle the bitwise operations mentioned earlier, they are in fact flexible, programmable state machines capable of performing more advanced transformations as well.

**Feature List**
- Two BitScramblers, one for RX (peripheral-to-memory), one for TX (memory-to-peripheral)
- Support for memory-to-memory transfers
- Processing up to 32 bits per DMA clock period
- Data path controlled by a BitScrambler program stored in instruction memory
- Input registers able to read 0, 8, 16, or 32 bits per clock cycle

**Output registers:**
- Able to write 0, 8, 16, or 32 bits per clock cycle
- Data sources for output register bits: 64 bits of input data, two counters, LUT RAM data, data output of last cycle, comparators.
- With some restrictions, each of the 32 output registers can come from any bit on the data sources

An 8 x 257-bit instruction memory for storing eight instructions, controlling control flow, and the data path
- 2048 bytes of lookup table (LUT) memory, configurable as various word widths

**Pin Assignment**
The BitScrambler does not directly interact with IOs, so it has no pins assigned.

---

### **4.2.3 Analog Signal Processing**

This subsection describes components on the chip that sense and process real-world data.

#### 4.2.3.1 Touch Sensor

ESP32-P4 has 14 capacitive-sensing GPIOs, which detect variations induced by touching or approaching the GPIOs with a finger or other objects. The low-noise nature of the design and the high sensitivity of the circuit allow relatively small pads to be used. Arrays of pads can also be used, so that a larger area or more points

---

**Footer:**
Espressif Systems  
ESP32-P4 Series Datasheet v0.6  
Submit Documentation Feedback