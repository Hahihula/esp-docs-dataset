

```markdown
In Joint Download Boot mode, users can download binary files into flash using UART0, USB or SDIO Slave interface. It is also possible to download binary files into SRAM and execute it from SRAM.

Figure 8.2-1 shows the detailed boot flow of the chip.
```

![Figure 8.2-1. Chip Boot Flow](image)

```markdown
Notice: The strapping values "1xxx" and "01xx" in the above figure are the combination of GPIO9 and GPIO8. See Table 8.2-2.
```

The following eFuses control boot mode behaviors:

*   **EFUSE_DIS_FORCE_DOWNLOAD**
    - If this eFuse is 0 (default), software can force switch the chip from SPI Boot mode to Joint Download Boot mode by setting register LP_AON_FORCE_DOWNLOAD_BOOT and triggering a CPU reset. In this case, hardware overwrites GPIO_STRAPPING[3:2] from "1x" to "01".
```