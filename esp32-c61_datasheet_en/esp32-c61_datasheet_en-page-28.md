**Title: Boot Configurations**

---

### Table 3-2. Description of Timing Parameters for the Strapping Pins

| Parameter | Description                                                                                   | Min (ms) |
|-----------|--------------------------------------------------------------------------------------------------|----------|
| tSU       | Setup time is the time reserved for the power rails to stabilize before the CHIP PU pin is pulled high to activate the chip. | 0        |
| tH        | Hold time is the time reserved for the chip to read the strapping pin values after CHIP PU is already high and before these pins start operating as regular IO pins. | 3        |

**Figure Caption:**
- Figure 3-1. Visualization of Timing Parameters for the Strapping Pins

---

### Section Title:
#### Chip Boot Mode Control (3.1)

GPIO8 and GPIO9 control the boot mode after the reset is released. See Table 3-3 Chip Boot Mode Control.

**Table 3-3. Chip Boot Mode Control**

| Boot Mode | GPIO8   | GPIO9    |
|-----------|---------|----------|
| SPI Boot  | Any value | 1        |
| Joint Download Boot | Bold marks the default value and configuration. |

Joint Download Boot mode supports the following download methods:

- USB-Serial-JTAG Download Boot
- UART Download Boot
- SDIO Slave 2.0 Download Boot

In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system.

In Joint Download Boot mode, users can download binary files into flash using UARTO, USB or SDIO Slave interfaces and execute it in SPI Boot mode.

---

**Footer:**
- Page 28
- Espressif Systems ESP32-C61 Series Datasheet v0.5