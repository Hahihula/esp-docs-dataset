**Title: Boot Configurations**

---

### Table 3-2. Description of Timing Parameters for the Strapping Pins

| Parameter | Description                                                                                   | Min (ms) |
|-----------|--------------------------------------------------------------------------------------------------|----------|
| tSU       | Setup time is the time reserved for the power rails to stabilize before the CHIP_PU pin is pulled high to activate the chip. | 0        |
|           | Hold time is the time reserved for the chip to read the strapping pin value after CHIP_PU is already high and before these pins start operating as regular IO pins. |            |
| tH        |                                                                                                 | 3        |

**Figure Caption:**
- Figure 3-1. Visualization of Timing Parameters for the Strapping Pins

---

### Section Title:
#### Chip Boot Mode Control
##### Subsection:

GPI035–GPIO38 control the boot mode after the reset is released. See Table 3-3 Chip Boot Mode Control.

**Table Caption:**
- Table 3-3. Boot Mode Control

| Boot Mode       | GPIO35   | GPIO36    | GPIO37^3 | GPIO38^3 |
|-----------------|----------|-----------|----------|----------|
| SPI Boot        | 1        | Any value | Any value| Any value|
| Joint Download Boot^2 | 0      | 1         | Any value| Any value|

**Table Notes:**
1. Bold marks the default value and configuration.
2. Joint Download Boot mode supports the following download methods:
   - USB Download Boot:
     - USB-Serial-JTAG Download Boot
     - USB 2.0 OTG Download Boot
   - UART Download Boot
   - SPI Slave Download Boot

3. For details about the functionalities of GPIO37 and GPIO38, see ESP32-P4 Technical Reference Manual > Chapter Chip Boot Control.

---

**Additional Information:**
In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system.
- **Footer:** 
  - Page Number: 34
  - Document Title: ESP32-P4 Series Datasheet v0.6

--- 

[Submit Documentation Feedback]