

```markdown
- Arithmetic, logical, AIA instructions
- Zc-extension instructions
- Any interrupts/exceptions within the HWLP
- ECALL/EBREAK
- FENCE/FENCE.I/CSRx instructions
- Atomic instructions
- Debug mode
- Data address in SC.W instruction not matching that in LR.W instruction

### 1.71.5 HWLP Constraints

Please note that branch or jump instructions at the end of HWLP may cause unexpected behavior.

### 1.71.6 Register Summary

| Name                        | Description                          | Address | Access |
|-----------------------------|--------------------------------------|---------|--------|
| mhwloop0_start_addr         | Machine Loop0 start address          | 0x7C6   | R/W    |
| mhwloop0_end_addr           | Machine Loop0 end address            | 0x7C7   | R/W    |
| mhwloop0_count              | Machine Loop0 count                  | 0x7C8   | R/W    |
| mhwloop1_start_addr         | Machine Loop1 start address          | 0x7C9   | R/W    |
| mhwloop1_end_addr           | Machine Loop1 end address            | 0x7CA   | R/W    |
| mhwloop1_count              | Machine Loop1 count                  | 0x7CB   | R/W    |
| mex_t_ill_reg               | Machine extension illegal register   | 0x7F0   | R/W    |
| mhwloop_state_reg           | Machine HWLP state register          | 0x7F1   | R/W    |
| uhwloop0_start_addr         | User Loop0 start address             | 0x8C0   | R/W    |
| uhwloop0_end_addr           | User Loop0 end address               | 0x8C1   | R/W    |
| uhwloop0_count              | User Loop0 count                     | 0x8C2   | R/W    |
| uhwloop1_start_addr         | User Loop1 start address             | 0x8C3   | R/W    |
| uhwloop1_end_addr           | User Loop1 end address               | 0x8C4   | R/W    |
| uhwloop1_count              | User Loop1 count                     | 0x8C5   | R/W    |
| uhwloop_state_reg           | User HWLP state register             | 0x8C6   | R/W    |

### 1.71.7 Register Description

**Register 1.79. mhwloop0_start_addr (0x7C6)**

```
31                                                                                       0
+--------------------------------------------------------------------------------------------------+
| 0x00000000                                                                                      | Reset |
+--------------------------------------------------------------------------------------------------+

SA Configures the 32-bit address of the first instruction of HW Loop0. Valid when mh-wloop_state_reg.STATE is not 0x0, that is, not OFF. (R/W)
```
```