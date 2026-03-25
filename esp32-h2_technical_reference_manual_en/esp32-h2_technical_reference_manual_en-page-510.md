

```markdown
- Invalidate write operations
    * Triggers interrupt

The APM controller will automatically record relevant information about the illegal access, including the master ID, security mode, access address, reasons for illegal access (address out of bounds or permission restrictions), and permission management result of each access path. All these information can be obtained from relevant registers listed in Section 15.7 Register Summary.

Take the access path HP_APM_CTRL MO as an example. When illegal access occurs:

* `HP_APM_MO_EXCEPTION_ID` records the master ID.
* `HP_APM_MO_EXCEPTION_MODE` records the security mode.
* `HP_APM_MO_EXCEPTION_ADDR` records the access address.
* `HP_APM_MO_EXCEPTION_STATUS` records the reason for illegal access.

    - If the address requested to access is not within the enabled address ranges, bit1 will be set to 1, indicating the address is out of bounds.
    - If the address requested to access is within the enabled address ranges, but the master does not have the read/write/execute permission within this region, then bit0 will be set to 1, indicating permission restrictions.

* `HP_APM_MO_EXCEPTION_REGION` records the permission management result of each address range. This register has a total of 16 bits, corresponding to 16 address ranges, and bit0 corresponds to the first address range. When the address to access is within a particular enabled address range, but the master does not have the corresponding read/write/execute permission within this address range, the corresponding bit of this register will be set to 1.

ESP32-H2’s APM controller can generate five interrupt signals, which will be sent to Interrupt Matrix (INTMTX):

* `HP_APM_MO_INTR`
* `HP_APM_M1_INTR`
* `HP_APM_M2_INTR`
* `HP_APM_M3_INTR`
* `LP_APM_MO_INTR`

These five interrupt signals correspond to the controlled access paths shown in Figure 15.4-1. If an illegal access occurs in a controlled access path, the corresponding interrupt will be generated.

## 15.7 Register Summary

### 15.7.1 APM Registers of HP System (HP_APM_REG)

The addresses in this section are relative to the Access Permission Management Controller (HP_APM) base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```