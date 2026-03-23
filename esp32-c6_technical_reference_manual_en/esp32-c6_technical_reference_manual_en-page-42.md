

```markdown
| Name          | Description                                      | Address   | Access |
|---------------|--------------------------------------------------|-----------|--------|
| pmpcf g3      | Physical memory protection configuration         | 0x3A3     | R/W    |
| pmpaddr0      | Physical memory protection address register      | 0x3B0     | R/W    |
| pmpaddr1      | Physical memory protection address register      | 0x3B1     | R/W    |
|               |                                                  | ...       |        |
| pmpaddr15     | Physical memory protection address register      | 0x3BF     | R/W    |

**Trigger Module CSRs (shared with Debug Mode)**

| Name          | Description                  | Address   | Access |
|---------------|------------------------------|-----------|--------|
| tselect       | Trigger Select Register      | 0x7A0     | R/W    |
| tdata1        | Trigger Abstract Data 1      | 0x7A1     | R/W    |
| tdata2        | Trigger Abstract Data 2      | 0x7A2     | R/W    |
| tcontrol      | Global Trigger Control       | 0x7A5     | R/W    |

**Debug Mode CSRs**

| Name          | Description                  | Address   | Access |
|---------------|------------------------------|-----------|--------|
| dcsr          | Debug Control and Status     | 0x7B0     | R/W    |
| dpc           | Debug PC                     | 0x7B1     | R/W    |
| dscratch0     | Debug Scratch Register 0     | 0x7B2     | R/W    |
| dscratch1     | Debug Scratch Register 1     | 0x7B3     | R/W    |

**Performance Counter CSRs (Custom)**⁴

| Name          | Description                  | Address   | Access |
|---------------|------------------------------|-----------|--------|
| mpcer          | Machine Performance Counter Event | 0x7E0     | R/W    |
| mpcmr          | Machine Performance Counter Mode | 0x7E1     | R/W    |
| mpccr          | Machine Performance Counter Count | 0x7E2     | R/W    |

**GPIO Access CSRs (Custom)**

| Name          | Description                  | Address   | Access |
|---------------|------------------------------|-----------|--------|
| cpu_gpio_oen  | GPIO Output Enable           | 0x803     | R/W    |
| cpu_gpio_in   | GPIO Input Value             | 0x804     | RO     |
| cpu_gpio_out  | GPIO Output Value            | 0x805     | R/W    |

**Physical Memory Attributes Checker (PMAC) CSRs**

| Name          | Description                  | Address   | Access |
|---------------|------------------------------|-----------|--------|
| pma_cfg0      | Physical memory attribute configuration | 0xBC0     | R/W    |
| pma_cfg1      | Physical memory attribute configuration | 0xBC1     | R/W    |
| pma_cfg2      | Physical memory attribute configuration | 0xBC2     | R/W    |
| pma_cfg3      | Physical memory attribute configuration | 0xBC3     | R/W    |
|               | ...                          |           |        |
| pma_cfg15     | Physical memory attribute configuration | 0xBCF     | R/W    |
| pma_addr0     | Physical memory attribute address register | 0xBD0     | R/W    |
| pma_addr1     | Physical memory attribute address register | 0xBD1     | R/W    |
|               | ...                          |           |        |
| pma_addr15    | Physical memory attribute address register | 0xBDF     | R/W    |

Note that if write/set/clear operation is attempted on any of the CSRs which are read-only (RO), as indicated in the above table, the CPU will generate illegal instruction exception.
```