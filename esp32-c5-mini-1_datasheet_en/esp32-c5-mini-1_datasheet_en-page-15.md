**Title: Boot Configurations**

---

### Table 4-3. Boot Mode Control

| Boot Mode | GPIO26 | GPIO27 | GPIO28 |
|-----------|--------|--------|--------|
| SPI Boot^1| Any value | Any value | 1      |
| Joint Download Boot O^2| Any value | 1       | 0      |
| Joint Download Boot ^3| 0        | 0       | 0      |

**Note:**
1. Bold marks the default value and configuration.

#### Joint Download Boot O mode supports:
- USB-Serial-JTAG Download Boot
- UART Download Boot

#### SPI Slave Download Boot (chip revision v0.1 only)
- Joint Download Boot ^3 mode supports:

##### load methods:
- UART Download Boot
- SDIO Download Boot

In **SPI Boot** mode, the ROM bootloader loads and executes the program from SPI flash to boot the system.

In *Joint Download* Boot O mode, users can download binary files into flash using UARTO, USB, or SPI Slave interfaces. It is also possible to download binary files into SRAM and execute it from SRAM.
In Joint Download Boot ^3 mode, users can download binary files into flash using UARTO or SDIO interfaces. It is also possible to download binary files into SRAM and execute it from SRAM.

---

### 4.2 SDIO Sampling and Driving Clock Edge Control

The strapping pin GPIO25 and MTDI can be used to decide on which clock edge to sample signals and drive output lines. See Table **4-4** for details:

| Edge behavior | GPIO25 | MTDI |
|----------------|--------|------|
| Falling edge sampling, falling edge output | 0      | 0    |
| Rising edge sampling, rising edge output   | 1      | 0    |
| Rising edge sampling, rising edge output   | 1      | 1    |

**Note:**
1. GPIO25 and MTDI are floating by default; therefore above configurations.

---

### 4.3 ROM Messages Printing Control

During the boot process, messages from the ROM code can be printed to:
- (Default) UARTO and USB Serial/JTAG controller
- UARTO

---

**Footer:**
Espressif Systems  
15  
ESP32-C5-MINI-1 Datasheet v1.0  

[Submit Documentation Feedback](#)