

```markdown
In SPI Download Boot mode, users can download binary files into flash using SPI interface. It is also possible to download binary files into SRAM and execute it from SRAM.

Figure 8.2-1 shows the detailed boot flow of the chip.
```

![Figure 8.2-1. Chip Boot Flow](image)

```markdown
*Note: The strapping values "1xxx" and "01xx/0001" are the combination of GPIO9, GPIO8, GPIO3 and GPIO2 pins, see Table 8.2-2.
```

The following eFuses control boot mode behaviors:

*   **EFUSE_DIS_FORCE_DOWNLOAD**
    - If this eFuse is 0 (default), software can force switch the chip from SPI Boot mode to Joint Download Boot mode by setting register `LP_AON_FORCE_DOWNLOAD_BOOT` and triggering a CPU reset. In this case, hardware overwrites `GPIO_STRAPPING[3:2]` from "1x" to "01".
```

```markdown
Chapter 8 Chip Boot Control GoBack

In SPI Download Boot mode, users can download binary files into flash using SPI interface. It is also possible to download binary files into SRAM and execute it from SRAM.

Figure 8.2-1 shows the detailed boot flow of the chip.
```

```mermaid
flowchart TD
    A[Reset] --> B{Check Strapping Value*}
    B -- Yes --> C[Check binary header]
    C --> D{EFUSE_DIS_DIRECT_BOOT == 0 & Header == 0xaedb041d}
    D -- Yes --> E[Initialization<br>Enable cache and set up MMU]<br><br>Jump to entry point in flash
    D -- No --> F[Initialization]<br>Copy the program from flash to RAM<br><br>Jump to entry Point in RAM
    B -- No --> G[Initialization]
    G --> H{(01xx):Wait for downloading from UART0/USB<br>(0001): Wait for downloading from SPI}
```

```markdown
Figure 8.2-1. Chip Boot Flow

*Note: The strapping values "1xxx" and "01xx/0001" are the combination of GPIO9, GPIO8, GPIO3 and GPIO2 pins, see Table 8.2-2.
```

```markdown
The following eFuses control boot mode behaviors:

*   **EFUSE_DIS_FORCE_DOWNLOAD**
    - If this eFuse is 0 (default), software can force switch the chip from SPI Boot mode to Joint Download Boot mode by setting register `LP_AON_FORCE_DOWNLOAD_BOOT` and triggering a CPU reset. In this case, hardware overwrites `GPIO_STRAPPING[3:2]` from "1x" to "01".
```

```markdown
Espressif Systems 347 ESP32-H2 TRM (Version 1.1)
Submit Documentation Feedback
```