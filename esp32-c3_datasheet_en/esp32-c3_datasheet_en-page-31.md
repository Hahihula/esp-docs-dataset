**Title: Boot Configurations**

---

**Figure Caption:**  
Figure 3-1. Visualization of Timing Parameters for the Strapping Pins

---

**Subtitle:**  
3.1 Chip Boot Mode Control

**Body Text:**  
GPI02, GPI08, and GPIO9 control the boot mode after the reset is released. See Table 3-3 Chip Boot Mode Control.

---

**Table Title:**  
Table 3-3. Chip Boot Mode Control

| Boot Mode       | GPIO2^1 | GPIO8 | GPIO9 |
|-----------------|--------|-------|-------|
| SPI boot mode   | 1      | Any value | 1     |
| Joint download boot mode | 1    | 1        | 0     |

**Table Notes:**  
1. Bold marks the default value and configuration.
2. GPIO2 actually does not determine SPI Boot and Joint Download Boot mode, but it is recommended to pull this pin up due to glitches.

---

**Body Text Continued:**

Joint Download Boot mode supports the following download methods:

- USB-Serial-JTAG Download Boot
- UART Download Boot

In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system. 

In Joint Download Boot mode, users can download binary files into flash using UARTO or USB interface. It is also possible to download binary files into SRAM and execute it from SRAM.

In addition to SPI Boot and Joint Download Boot modes, ESP32-C3 also supports SPI Download Boot mode.
For details, please see [ESP32-C3 Technical Reference Manual > Chapter Chip Boot Control](#).

---

**Subtitle:**  
3.2 ROM Messages Printing Control

**Body Text Continued:**

During the boot process, the messages by the ROM code can be printed to:

- (Default) UARTO and USB Serial/JTAG controller

---

**Footer Information:**  
Espressif Systems  
Page 31  
ESP32-C3 Series Datasheet v2.2  

[Submit Documentation Feedback](#)