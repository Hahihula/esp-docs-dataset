**Title: Boot Configurations**

---

### Table 4-2: Description of Timing Parameters for the Strapping Pins

| Parameter | Description                                                                                   | Min (ms) |
|-----------|--------------------------------------------------------------------------------------------------|----------|
| tSU       | Setup time is the time reserved for the power rails to stabilize before the CHIP_EN pin is pulled high to activate the chip. | 0        |
| tH        | Hold time is the time reserved for the chip to read the strapping pin values after CHIP_EN is already high and before these pins start operating as regular IO pins. | 3        |

![Figure 4-1](#) Visualization of Timing Parameters for the Strapping Pins

---

### Section: Chip Boot Mode Control (4.1)

GPIO2, GPIO8, and GPIO9 control the boot mode after the reset is released. See Table [4-3](#) Chip Boot Mode Control.

#### Table 4-3: Chip Boot Mode Control

| Boot Mode       | GPIO2^2 | GPIO8   | GPIO9 |
|-----------------|---------|---------|-------|
| SPI boot mode   | 1       | Any value | 1     |
| Joint download boot mode | 1      | 1       | 0     |

1. Bold marks the default value and configuration.
2. GPIO2 actually does not determine SPI Boot and Joint Down-load Boot mode, but it is recommended to pull this pin up due to glitches.

#### Joint Download Boot mode supports the following download methods:

- USB-Serial-JTAG Download Boot
- UART Download Boot

In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system. 

---

**Footer:**
Espressif Systems  
13 ESP32-C3-WROOM-02 & WROOM-02U Datasheet v1.6  
[Submit Documentation Feedback](#)