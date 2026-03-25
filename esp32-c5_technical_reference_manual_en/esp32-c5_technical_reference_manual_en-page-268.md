

# 7.6 Registers

The addresses in this section are relative to eFuse controller base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 7.1. EFUSE_PGM_DATA_n_REG (n: 0-7) (0x0000+0x4*n)

EFUSE_PGM_DATA_n Configures the nth 32-bit data to be programmed. (R/W)

## Register 7.2. EFUSE_PGM_CHECK_VALUE_n_REG (n: 0-2) (0x0020+0x4*n)

EFUSE_PGM_RS_DATA_n Configures the nth RS code to be programmed. (R/W)

## Register 7.3. EFUSE_RD_WR_DIS_REG (0x002C)

EFUSE_WR_DIS Represents whether programming of individual eFuse memory bit is disabled. For mapping between the bits of this field and the eFuse memory bits, please refer to Table 7.3-1 and Table 7.3-3.

1: Disabled  
0: Enabled (RO)