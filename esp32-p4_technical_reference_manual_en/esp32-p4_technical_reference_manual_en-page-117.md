

```markdown
Register 1.89. uhwloop0_count (0x8C2)

| 31 | 24 | 23 | 0 |
|-----:|----:|----:|---|
|    0x00 |        | 0x000000 | Reset |

Count Configures the number of iterations of HW Loop0 in user mode. Valid when mh-wloop_state_reg.STATE is not 0x0, that is, not OFF. It is read-writable only when mh-wloop_state_reg.URW is 1. (R/W)

Register 1.90. uhwloop1_start_addr (0x8C3)

| 31 | 0 |
|-----:|---|
|    0x00000000 | Reset |

SA Configures the 32-bit address of the first instruction of HW Loop1 in user mode. Valid when mhwloop_state_reg.STATE is not 0x0, that is, not OFF. It is read-writable only when mh-wloop_state_reg.URW is 1. (R/W)

Register 1.91. uhwloop1_end_addr (0x8C4)

| 31 | 0 |
|-----:|---|
|    0x00000000 | Reset |

EA Configures the 32-bit address of the last instruction of HW Loop1 in user mode. Valid when mhwloop_state_reg.STATE is not 0x0, that is, not OFF. It is read-writable only when mh-wloop_state_reg.URW is 1. (R/W)

Register 1.92. uhwloop1_count (0x8C5)

| 31 | 24 | 23 | 0 |
|-----:|----:|----:|---|
|    0x00 |        | 0x000000 | Reset |

Count Configures the number of iterations of HW Loop1 in user mode. Valid when mh-wloop_state_reg.STATE is not 0x0, that is, not OFF. It is read-writable only when mh-wloop_state_reg.URW is 1. (R/W)
```