
```markdown
Register 4.102. EFUSE_RD_RS_ERR1_REG (0x01C4)

EFUSE_KEY5_ERR_NUM The value of this signal means the number of error bytes. (RO)

EFUSE_KEY4_FAIL 0: Means no failure and that the data of KEY4 is reliable 1: Means that programming KEY4 data failed and the number of error bytes is over 6. (RO)

EFUSE_SYS_PART2_ERR_NUM The value of this signal means the number of error bytes. (RO)

EFUSE_KEY5_FAIL 0: Means no failure and that the data of KEY5 is reliable 1: Means that programming KEY5 data failed and the number of error bytes is over 6. (RO)

Register 4.103. EFUSE_CLK_REG (0x01C8)

EFUSE_EFUSE_MEM_FORCE_PD Set this bit to force eFuse SRAM into power-saving mode. (R/W)

EFUSE_MEM_CLK_FORCE_ON Set this bit and force to activate clock signal of eFuse SRAM. (R/W)

EFUSE_EFUSE_MEM_FORCE_PU Set this bit to force eFuse SRAM into working mode. (R/W)

EFUSE_CLK_EN Set this bit and force to enable clock signal of eFuse memory. (R/W)
```