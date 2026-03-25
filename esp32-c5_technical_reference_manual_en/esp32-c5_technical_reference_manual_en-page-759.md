

# 18.9 Registers

## 18.9.1 HP_APM_REG

The addresses in this section are relative to the HP_APM base address provided in Table 6.3-2 in Chapter 6 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

Register 18.1. HP_APM_REGION_FILTER_EN_REG (0x0000)

HP_APM_REGION_FILTER_EN Configure bit n (0-15) to enable permission checks for region n (0-15).
O: Disable
1: Enable
(R/W)

Register 18.2. HP_APM_REGIONn_ADDR_START_REG (n: 0-15) (0x0004+0xC*n)

HP_APM_REGIONn_ADDR_START Configures the start address of region n. (R/W)