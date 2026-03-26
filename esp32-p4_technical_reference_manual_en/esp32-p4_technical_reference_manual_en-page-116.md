

```markdown
Register 1.86. mhwloop_state_reg (0x7F1)

31                                 3   2   1   0
-----------------------------------------------
| (reserved)                        URW STATE |
-----------------------------------------------
0x00000000    | 0x0  0x0 |

STATE Configures the state of the HWLP extension.
Ox0: OFF (Accessing HWLP instructions and CSRs will trigger an illegal instruction exception)
Ox1: INITIAL
Ox2: CLEAN
Ox3: DIRTY
(R/W)

URW Configures user-mode access for user-mode HWLOOP CSRs.
0: User-mode access is disabled
1: User-mode access is enabled
(R/W)


Register 1.87. uhwloopO_start_addr (0x8C0)

31                                 0
-----------------------------------------------
| (reserved)                        |
-----------------------------------------------
0x00000000    | Reset |

SA Configures the 32-bit address of the first instruction of HW LoopO in user mode. Valid when mhwloop_state_reg.STATE is not Ox0, that is, not OFF. It is read-writable only when mh-wloop_state_reg.URW is 1. (R/W)


Register 1.88. uhwloopO_end_addr (0x8C1)

31                                 0
-----------------------------------------------
| (reserved)                        |
-----------------------------------------------
0x00000000    | Reset |

EA Configures the 32-bit address of the last instruction of HW LoopO in user mode. Valid when mhwloop_state_reg.STATE is not Ox0, that is, not OFF. It is read-writable only when mh-wloop_state_reg.URW is 1. (R/W)
```