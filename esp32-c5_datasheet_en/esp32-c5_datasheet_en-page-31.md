**Title: Boot Configurations**

---

### Table 3-3. Boot Mode Control

| Boot Mode | GPIO26 | GPIO27 | GPIO28 |
|-----------|--------|--------|--------|
| SPI Boot¹ | Any value | Any value | 1      |
| Joint Download Boot O² | Any value | 1       | 0      |
| Joint Download Boot I³ | 0        | 0       | 0      |

**Footnotes:**
1. Bold marks the default value and configuration.
2. Joint Download Boot mode supports the following download methods:
   - USB-Serial-JTAG Download Boot
   - UART Download Boot
3. SPI Slave Download Boot (chip revision v0.1 only)
4. Joint Download Boot 1 mode supports the following download methods:
   - UART Download Boot
   - SDIO Download Boot

**Body Text:**
In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system.

In Joint Download Boot O mode, users can download binary files into flash using UARTO, USB, or SPI Slave interfaces. It is also possible to download binary files into SRAM and execute it from SRAM.

In Joint Download Boot I mode, users can download binary files into flash using UARTO or SDIO interfaces. It is also possible to download binary files into SRAM and execute it from SRAM.

---

### 3.2 SDIO Sampling and Driving Clock Edge Control

The strapping pin GPIO25 and MTDI can be used to decide on which clock edge to sample signals and drive output lines. See Table 3-4 SDIO Input Sampling Edge/Output Driving Edge Control.

**Table:**
| | GPIO25 | MTDI |
|---|--------|------|
| Falling edge sampling, falling edge output | O      |       |
| Rising edge sampling, rising edge output   |       | 1     |

---

### 3.3 ROM Messages Printing Control

During the boot process, the messages by the ROM code can be printed to:
- (Default) UARTO and USB Serial/JTAG controller
- UARTO

---

**Footer:**
Espressif Systems  
ESP32-C5 Series Datasheet v1.0  
Submit Documentation Feedback