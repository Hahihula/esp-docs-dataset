

```markdown
In Joint Download Boot 1 mode, users can download binary files into flash using UART0 or SDIO interfaces. It is also possible to download binary files into SRAM and execute it from SRAM.

Figure 10.2-1 Chip Boot Flow shows the detailed boot flow of the chip.
```

![Figure 10.2-1. Chip Boot Flow](image_path)

```markdown
The following eFuse parameters control boot mode behaviors:

*   **EFUSE_DIS_FORCE_DOWNLOAD**
    - If this eFuse is 0 (default), software can force switch the chip from SPI Boot mode to Joint Download Boot mode by setting register LP_AON_FORCE_DOWNLOAD_BOOT and triggering a CPU reset. In this case, hardware overwrites GPIO_STRAPPING[4:3] from "1x" to "01".
    - If this eFuse is 1, LP_AON_FORCE_DOWNLOAD_BOOT is disabled, and GPIO_STRAPPING can not be overwritten.
*   **EFUSE_DIS_DOWNLOAD_MODE**
```

```markdown
Espressif Systems

Submit Documentation Feedback
```