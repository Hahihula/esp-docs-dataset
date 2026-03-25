

```markdown
## 8.2.1 Default Configuration

By default, GPIO9 is connected to the chip's internal pull-up resistor. If GPIO9 is not connected or is connected to an external high-impedance circuit, the internal weak pull-up determines the default input level of this strapping pin (see Table 8.2-1).

Table 8.2-1. Default Configuration of Strapping Pins

| Strapping Pin | Default Configuration |
|---------------|------------------------|
| MTMS          | Floating               |
| MTDI          | Floating               |
| GPIO7         | Floating               |
| GPIO8         | Floating               |
| GPIO9         | Pull-up                |

To change the strapping bit values, users can apply external pull-down/pull-up resistors, or use host MCU GPIOs to control the voltage level of these pins when powering on ESP32-C61. After the reset is released, the strapping pins work as normal-function pins.

## 8.2.2 Boot Mode Control

The values of GPIO9 and GPIO8 at reset determine the boot mode after the reset is released. Table 8.2-2 shows the strapping pin values of GPIO9 and GPIO8, and the associated boot modes.

Table 8.2-2. Boot Mode Control

| Boot Mode             | GPIO9 | GPIO8 |
|-----------------------|-------|-------|
| SPI Boot mode         | 1     | x¹    |
| Joint Download Boot mode² | 0     | 1     |

---

¹x: values that have no effect on the result and can therefore be ignored.
²Joint Download Boot mode: Joint Download Boot mode supports the following download methods:
- USB-Serial-JTAG Download Boot
- UART Download Boot
- SDIO Slave 2.0 Download Boot

In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system.  
SPI Boot mode can be further classified as follows:

- **Normal Flash Boot**: supports Secure Boot. The ROM bootloader loads the program from flash into SRAM and executes it. In most practical scenarios, this program is the 2nd stage bootloader, which later boots the target application.
- **Direct Boot**: does not support Secure Boot and programs run directly from flash. To enable this mode, make sure that the first two words of the bin file downloaded to flash are `0xaeddb041d`. For more detailed process, see Figure 8.2-1.
```