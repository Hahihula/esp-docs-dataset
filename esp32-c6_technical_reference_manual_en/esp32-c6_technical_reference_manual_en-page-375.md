

```markdown
Table 9.2-1. Default Configuration of Strapping Pins

| Strapping Pin | Default Configuration |
|---------------|------------------------|
| MTMS          | Floating               |
| MTDI          | Floating               |
| GPIO8         | Floating               |
| GPIO9         | Pull-up                |
| GPIO15        | Floating               |

Table 9.2-2. Boot Mode Control

| Boot Mode   | GPIO9 | GPIO8 |
|-------------|-------|-------|
| SPI Boot    | 1     | x     |
| Download Boot | 0     | 1     |

* x: this value is ignored.
```

In SPI Boot mode, the ROM bootloader loads and executes the program from SPI flash to boot the system. SPI Boot mode can be further classified as follows:

- Normal Flash Boot: supports Secure Boot. The ROM bootloader loads the program from flash into SRAM and executes it. In most practical scenarios, this program is the 2nd stage bootloader, which later boots the target application.
- Direct Boot: does not support Secure Boot and programs run directly from flash. To enable this mode, make sure that the first two words of the bin file downloaded to flash are 0xaedb041d. For more detailed process, see Figure 9.2-1.

In Download Boot mode, users can download code into flash using UART0 or USB interface. It is also possible to load a program into SRAM and execute it from SRAM.

Figure 9.2-1 shows the detailed boot flow of the chip.
```