

```markdown
Chapter 18 Permission Control (PMS)

GoBack

18.6 Illegal Access and Interrupts

18.6.1 SYS_APM Controller

When the information carried on the bus does not match the configuration, ESP32-C5 treats it as an illegal access and handles it as follows:

* Rejects the access request and returns a default value, specifically:
    - Returns 0 for read and execute operations
    - Ignores write operations
* Triggers interrupt

The SYS_APM controller will automatically record information related to the illegal access, including the master ID, security mode, access address, reasons for illegal access (address out of bounds or permission restrictions), and permission management result of each access path. All this information can be obtained from relevant registers listed in Section 18.8 Register Summary.

Take the access path HP_APM_CTRL MO as an example. When an illegal access occurs:

* `HP_APM_MO_EXCEPTION_ID` records the master ID.
* `HP_APM_MO_EXCEPTION_MODE` records the security mode.
* `HP_APM_MO_EXCEPTION_ADDR` records the access address.
* `HP_APM_MO_EXCEPTION_STATUS` records the reason for illegal access.

    - If the address requested to access is not within the enabled address ranges, bit 1 will be set to 1, indicating the address is out of bounds.
    - If the address requested to access is within the enabled address ranges, but the master does not have the read/write/execute permission within this region, then bit 0 will be set to 1, indicating permission restrictions.

* `HP_APM_MO_EXCEPTION_REGION` records the permission management result of each address range.
    This register has a total of 16 bits, corresponding to 16 address ranges, and bit 0 corresponds to the first address range. When the address to access is within a particular enabled address range, but the master does not have the corresponding read/write/execute permission within this address range, the corresponding bit of this register will be set to 1.

The SYS_APM controller can generate 12 interrupt signals, which will be sent to Interrupt Matrix:

* `HP_APM_MO_INTR`
* `HP_APM_M1_INTR`
* `HP_APM_M2_INTR`
* `HP_APM_M3_INTR`
* `HP_APM_M4_INTR`
* `LP_APM_MO_INTR`
* `LP_APM_M1_INTR`

Espressif Systems
746
ESP32-C5 TRM (Version 1.0)

Submit Documentation Feedback
```