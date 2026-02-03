**Chapter Title:**
Chapter 8 Chip Boot Control

**GoBack Link:** GoBack

**Note Section:**
The following section provides description of the chip functions and the pattern of the strapping pins values to invoke each function. Only documented patterns should be used. If some pattern is not documented, it may trigger unexpected behavior.

**Section Title: 8.2 Boot Mode Control**

**Body Text:**
The values of GPIO0, GPIO1, GPIO2, and GPIO46 at reset determine the boot mode after the reset is released. Table 8.2-1 shows the strapping values of GPIO0, GPIO1, GPIO2, and GPIO46, and the associated boot modes.

**Table Title:**
Table 8.2-1. Boot Mode Control

| Boot Mode | GPIO0 | GPIO46 | GPIO1 | GPIO2 |
|-----------|-------|--------|-------|-------|
| SPI Boot mode | 1     | x      | x     | x     |
| Joint Download Boot mode^2 | 0    | 0      | X     | X     |
| SPI Download Boot mode^3 | 0    | 1      |       | O     |

**Footnotes:**
1. x: values that have no effect on the result and can therefore be ignored.
2. Joint Download Boot mode: Joint Download Boot mode supports the following download methods:
   - USB Download
   - USB-Serial-JTAG Download Boot
   - USB-OTG Download Boot
   - UART Download Boot

**Additional Information:** 
3 SPI Download Boot mode: GPIO1 and GPIO2 are not strapping pins. But you need to reserve them when using SPI Download Boot mode. GPIO1 and GPIO2 are floating by default and are in a high-impedance state at reset.

In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system. SPI Boot mode can be further classified as follows:
- Normal Flash Boot: supports Security Boot. The ROM bootloader loads the program from flash into SRAM and executes it. In most practical scenarios, this program is the 2nd stage bootloader, which later boots the target application.
- Direct Boot: does not support Security Boot and programs run directly from flash. To enable this mode, make sure that the first two words of the bin file downloaded to flash (address: 0x42000000) are 0xaedb041d.

In Joint Download Boot mode, users can download binary files into flash using UARTO or USB interface. It is also possible to download binary files into SRAM and execute it in this mode.
In SPI Download Boot mode, users can download binary files into flash using SPI interface. It is also possible to download binary files into SRAM and execute it from SRAM.

**List of eFuses control boot mode behaviors:**
- EFUSE_DISFORCE DOWNLOAD

**Footer Information:** 
Espressif Systems
535 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback