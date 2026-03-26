

```markdown
- Direct Boot: does not support Secure Boot and programs run directly from flash. To enable this mode, make sure that the first two words of the bin file downloaded to flash are 0xaedb041d. For more detailed process, see Figure 11.2-1.

In Joint Download Boot mode, users can download binary files into flash using UARTO, SPI slave, USB 2.0 OTG or USB Serial/JTAG interface. It is also possible to download binary files into L2MEM and execute it from L2MEM.

In SPI Download Boot mode, users can download binary files into flash using SPI interface. It is also possible to download binary files into L2MEM and execute it from L2MEM.

Figure 11.2-1 shows the detailed boot flow of the chip.
```

![Figure 11.2-1. Chip Boot Flow](image)

```markdown
Note: "x1" and "01" are combination values of strapping pins GPIO35 and GPIO36, see Table 11.2-2.

The following eFuse bits allows controlling boot mode behaviors:

* EFUSE_DIS_FORCE_DOWNLOAD

If this eFuse is 0 (default), software can force switch the chip from SPI Boot mode to Joint Download
```