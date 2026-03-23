

```markdown
Figure 9.2-1. Chip Boot Flow

*Note: The strapping values "1x" and "01" are the combination of GPIO9 and GPIO8 pins, see Table 9.2-2.
```

The following eFuses allows controlling boot mode behaviors:

*   `EFUSE_DIS_FORCE_DOWNLOAD`
    - If this eFuse is 0 (default), software can force switch the chip from SPI Boot mode to Download Boot mode by setting register `LP_AON_FORCE_DOWNLOAD_BOOT` and triggering a CPU reset. In this case, hardware overwrites `GPIO_STRAPPING[3:2]` from "1x" to "01".
    - If this eFuse is 1, `LP_AON_FORCE_DOWNLOAD_BOOT` is disabled. `GPIO_STRAPPING` can not be overwritten.
*   `EFUSE_DIS_DOWNLOAD_MODE`
```