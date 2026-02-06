**Title:**
4 Boot Configurations

---

**Table Title:** Table 4-2. Description of Timing Parameters for the Strapping Pins

| Parameter | Description | Min (ms) |
|-----------|-------------|----------|
| tSU       | Setup time is the time reserved for the power rails to stabilize before the CHIP_EN pin is pulled high to activate the chip. | 0        |
|          | Hold time is the time reserved for the chip to read the strapping pin values after CHIP_EN is already high and before these pins start operating as regular IO pins. | -         |

**Figure Title:** Figure 4-1. Visualization of Timing Parameters for the Strapping Pins

---

**Subtitle:**
4.1 Chip Boot Mode Control

**Body Text:**
GPIO2, GPIO8, and GPIO9 control the boot mode after the reset is released. See Table 4-3 Chip Boot Mode Control.

**Table Title:** Table 4-3. Chip Boot Mode Control

| Boot Mode | GPIO02^2 | GPIO8 | GPIO9 |
|-----------|----------|-------|-------|
| SPI boot mode | 1        | Any value | 1     |
| Joint download boot mode ^3 | 1       | 1      | 0     |

**Footnotes:**
1. Bold marks the default value and configuration.
2. GPIO2 actually does not determine SPI Boot and Joint Down-load Boot mode, but it is recommended to pull this pin up due to glitches.
3. Joint Download Boot mode supports the following download methods:
   - USB-Serial-JTAG Download Boot
   - UART Download Boot

**Additional Information:**
In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system.

---

**Footer:** 
Espressif Systems  
13  
Submit Documentation Feedback  

ESP8685-WROOM-01 Datasheet v1.5