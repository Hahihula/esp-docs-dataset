

```markdown
| Strapping Pin | Default Configuration |
|---------------|------------------------|
| GPIO8         | Floating               |
| GPIO9         | Pull-up                |
| GPIO25        | Floating               |

## 8.2.2 Boot Mode Control

The values of GPIO9, GPIO8, GPIO3 and GPIO2 at reset determine the boot mode after the reset is released. Table 8.2-2 shows the strapping pin values of GPIO9, GPIO8, GPIO3 and GPIO2, and the associated boot modes.

Table 8.2-2. Boot Mode Control

| Boot Mode                  | GPIO9 | GPIO8 | GPIO3 | GPIO2 |
|----------------------------|-------|-------|-------|-------|
| SPI Boot mode              | 1     | x¹    | x     | x     |
| Joint Download Boot mode² | 0     | 1     | x     | x     |
| SPI Download Boot mode³   | 0     | 0     | 0     | 1     |
| Invalid Combination⁴      | 0     | 0     | x     | 0     |

¹ x: values that have no effect on the result and can therefore be ignored.
² Joint Download Boot mode: Joint Download Boot mode supports the following download methods:
    * USB-Serial-JTAG Download Boot
    * UART Download Boot
³ SPI Download Boot mode: GPIO3 and GPIO2 need to be reserved only when using SPI Download Boot mode. GPIO3 and GPIO2 are floating by default and are in a high-impedance state at reset.
⁴ Invalid Combination: This combination can trigger unexpected behavior and should be avoided.

In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system. SPI Boot mode can be further classified as follows:

* Normal Flash Boot: supports Secure Boot. The ROM bootloader loads the program from flash into SRAM and executes it. In most practical scenarios, this program is the 2nd stage bootloader, which later boots the target application.
* Direct Boot: does not support Secure Boot and programs run directly from flash. To enable this mode, make sure that the first two words of the bin file downloaded to flash are 0xaedbd041d. For more detailed process, see Figure 8.2-1.

In Joint Download Boot mode, users can download binary files into flash using UARTO or USB interface. It is also possible to download binary files into SRAM and execute it from SRAM.
```