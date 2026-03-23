

# 15.7 Registers

The addresses in this section are relative to the World Controller base address provided in Table 3.3-3 in Chapter 3 System and Memory.

## Register 15.1. WCL_Core_0_MTVEC_BASE_REG (0x0000)

```
WCL_CORE_0_MTVEC_BASE
31 ------------------------------------------------------------- 0
| Reset |
-------------------------------------------------------------
```

**WCL_CORE_0_MTVEC_BASE** Configures the MTVEC base address, which should be kept consistent with the MTVEC in RISC-V. (R/W)

## Register 15.2. WCL_Core_0_MSTATUS_MIE_REG (0x0004)

```
WCL_CORE_0_MSTATUS_MIE
31 ------------------------------------------------------------- 0
| Reset |
-------------------------------------------------------------
(reserved) 1
```

**WCL_CORE_0_MSTATUS_MIE** Write 1 to enable World Switch Log Table. Only when the bit is set, the world switching is recorded in the World Switch Log Table. This bit is cleared once CPU switches from the Non-secure World to Secure World. (R/W)

## Register 15.3. WCL_Core_0_ENTRY_CHECK_REG (0x0008)

```
WCL_CORE_0_ENTRY_CHECK
31 ------------------------------------------------------------- 0
| Reset |
-------------------------------------------------------------
0x000000
```

**WCL_CORE_0_ENTRY_CHECK** Write 1 to enable CPU switching from Non-secure World to Secure world upon the monitored addresses. (R/W)