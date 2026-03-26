

```markdown
Register 1.80. mhwloop0_end_addr (0x7C7)
EA Configures the 32-bit address of the last instruction of HW Loop0. Valid when mh-wloop_state_reg.STATE is not 0x0, that is, not OFF. (R/W)

Register 1.81. mhwloop0_count (0x7C8)
COUNT Configures the number of iterations of HW Loop0. Valid when mhwloop_state_reg.STATE is not 0x0, that is, not OFF. (R/W)

Register 1.82. mhwloop1_start_addr (0x7C9)
SA Configures the 32-bit address of the first instruction of HW Loop1. Valid when mh-wloop_state_reg.STATE is not 0x0, that is, not OFF. (R/W)

Register 1.83. mhwloop1_end_addr (0x7CA)
EA Configures the 32-bit address of the last instruction of HW Loop1. Valid when mh-wloop_state_reg.STATE is not 0x0, that is, not OFF. (R/W)
```