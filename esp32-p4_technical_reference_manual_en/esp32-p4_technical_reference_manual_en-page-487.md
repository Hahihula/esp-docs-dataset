

```markdown
the error message to the error report register. For detailed steps to read parameters, please refer to the Section 8.3.3.

Figure 8.3-1. Data Flow in eFuse

Data in eFuse memory is organized in 11 blocks (BLOCK0 ~ BLOCK10).

BLOCK0 holds most parameters for software and hardware uses.

Table 8.3-1 lists all the parameters accessible (readable and usable) to users in BLOCK0 and their offsets, bit widths, accessibility by hardware, write protection, and brief function description. For more description on the parameters, please click the link of the corresponding parameter in the table.

The EFUSE_WR_DIS parameter is used to disable write protection of other parameters. EFUSE_RD_DIS is used to disable read protection of BLOCK4 ~ BLOCK10. For more information on these two parameters, please see Section 8.3.1.1 and Section 8.3.1.2.
```