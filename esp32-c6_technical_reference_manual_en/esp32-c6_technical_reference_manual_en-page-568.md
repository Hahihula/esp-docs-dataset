

```markdown
range, but the master doesn't have the corresponding read/write/execute permission within this address range, the corresponding bit of this register will be set to 1.

ESP32-C6's APM controller can generate seven interrupt signals, which will be sent to Interrupt Matrix (INTMTX):

*   HP_APM_MO_INTR
*   HP_APM_M1_INTR
*   HP_APM_M2_INTR
*   HP_APM_M3_INTR
*   LP_APM_MO_INTR
*   LP_APM_M1_INTR
*   LP_APM_MO_INTR

These seven interrupt signals correspond to the controlled access paths shown in Figure 16.3-1. If an illegal access occurs in a controlled access path, the corresponding interrupt will be generated.

## 16.6 Register Summary

### 16.6.1 High Performance APM Registers (HP_APM_REG)

The addresses in this section are relative to the Access Permission Management Controller (HP_APM) base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```