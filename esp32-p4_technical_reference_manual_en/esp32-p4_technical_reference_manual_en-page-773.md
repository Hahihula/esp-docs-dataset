

```markdown
| Strapping Pin | Default Configuration |
|---------------|------------------------|
| GPIO34        | Floating               |
| GPIO35        | Pull-up                |
| GPIO36        | Floating               |
| GPIO37        | Floating               |
| GPIO38        | Floating               |

Table 11.2-1. Default Configuration of Strapping Pins

## 11.2.2 Boot Mode Control

The values of GPIO35, GPIO36, GPIO37 and GPIO38 at reset determine the boot mode after the reset is released. Table 11.2-2 shows the strapping pin values of GPIO35, GPIO36, GPIO37 and GPIO38 and the associated boot modes.

Table 11.2-2. Boot Mode Control

| Boot Mode | GPIO35 | GPIO36 | GPIO37 | GPIO38 |
|-----------|--------|--------|--------|--------|
| SPI Boot mode (default) | 1      | x¹     | x      | x      |
| Joint Download Boot mode² | 0      | 1      | x      | x      |
| SPI Download Boot mode³ | 0      | 0      | 0      | 1      |
| Invalid Combination⁴   | 0      | 0      | 1      | x      |
|           | 0      | 0      | 0      | 0      |

¹ x: values that have no effect on the result and can therefore be ignored.
² Joint Download Boot mode: Joint Download Boot mode supports the following download methods:
    * USB-Serial-JTAG Download Boot
    * UART Download Boot
    * SPI Slave Download Boot
    * USB 2.0 OTG Download Boot
³ SPI Download Boot mode: GPIO37 and GPIO38 need to be reserved only when using SPI Download Boot mode. GPIO37 and GPIO38 are floating by default and are in a high-impedance state at reset.
⁴ Invalid Combination: This combination can trigger unexpected behavior and should be avoided.

In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system. SPI Boot mode can be further classified as follows:
* Normal flash Boot: supports Secure Boot. The ROM bootloader loads the program from flash into L2MEM and executes it. In most practical scenarios, this program is the 2nd stage bootloader, which later boots the target application.
```