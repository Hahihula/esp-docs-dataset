

```markdown
Chapter 1 High-Performance CPU

Register 1.84. mhwloop1_count (0x7CB)

COUNT Configures the number of iterations of HW Loop1. Valid when mhwloop_state_reg.STATE is not 0x0, that is, not OFF. (R/W)

Register 1.85. next_ill_reg (0x7F0)

ILL_FPU Represents whether an illegal instruction is triggered due to the disabled F extension.
O: Not triggered
1: Triggered
(RO)

ILL_HWL Represents whether the illegal instruction is triggered due to the disabled HWLP extension.
O: Not triggered
1: Triggered
(RO)

ILL_PIE Represents whether the illegal instruction is triggered due to the disabled PIE extension.
O: Not triggered
1: Triggered
(RO)
```