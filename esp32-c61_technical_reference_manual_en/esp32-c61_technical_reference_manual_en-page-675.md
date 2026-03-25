

```markdown
- If the address requested to access is not within the enabled address ranges, bit 1 will be set to 1, indicating the address is out of bounds.
- If the address requested to access is within the enabled address ranges, but the master does not have the read/write/execution permission within this region, then bit 0 will be set to 1, indicating permission restrictions.

• HP_APM_MO_EXCEPTION_REGION records the permission management result of each address range. This register has a total of 16 bits, corresponding to 16 address ranges, and bit 0 corresponds to the first address range. When the address to access is within a particular enabled address range, but the master does not have the corresponding read/write/execute permission within this address range, the corresponding bit of this register will be set to 1.

ESP32-C61's APM controller can generate the following interrupt signals and send them to the Interrupt Matrix:

• HP_APM_MO_INTR
• HP_APM_M1_INTR
• HP_APM_M2_INTR
• HP_APM_M3_INTR
• LP_APM_MO_INTR
• CPU_APM_MO_INTR
• CPU_APM_M1_INTR

The interrupt signals correspond to the controlled access paths shown in Figure 16.5-1. If an illegal access occurs in a controlled access path, the corresponding interrupt will be generated.

## 16.8 Register Summary

### 16.8.1 HP_APM_REG

The addresses in this section are relative to the Access Permission Management Controller (HP_APM) base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```