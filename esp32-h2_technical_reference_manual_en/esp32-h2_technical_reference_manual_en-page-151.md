

```markdown
Figure 5.3-1. Data Flow in eFuse
```

Data in eFuse memory is organized in 11 blocks (BLOCK0 ~ BLOCK10).

BLOCK0 holds most parameters for software and hardware uses.

Table 5.3-1 lists all the parameters accessible (readable and usable) to users in BLOCK0, their offsets, bit widths, whether they directly drive hardware modules, write protection, and brief function description. For more description on the parameters, please click the corresponding link in the table.

The EFUSE_WR_DIS parameter is used to disable write protection of other parameters. EFUSE_RD_DIS is used to disable read protection of BLOCK4 ~ BLOCK10. For more information, please see Section 5.3.1.2 and Section 5.3.1.3.
```