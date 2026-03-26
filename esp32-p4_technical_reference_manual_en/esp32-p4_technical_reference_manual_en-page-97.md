

```markdown
Register 1.63. mext_ill (0x7F0)

| 31 | 3 | 2 | 1 | 0 |
|----|---|---|---|---|
|    | Ox0 | 0x0 | 0x0 | Reset |

PIE_ILL Represents whether an illegal instruction exception occurred due to the CPU attempting to execute instructions belonging to the disabled PIE extension. (R/W)

HWLP_ILL Represents whether an illegal instruction exception occurred due to CPU attempting to execute instructions belonging to the disabled HWLP extension. (R/W)

FP_ILL Represents whether an illegal instruction exception occurred due to the CPU attempting to execute instructions belonging to the disabled RV32F extension, i.e. mstatus.FS=0x0. (R/W)
```

```markdown
Register 1.64. mext_hwlp_status (0x7F1)

| 31 | 3 | 2 | 1 | 0 |
|----|---|---|---|---|
|    | 0x000000 | 0x0 | 0x0 | Reset |

URW Represents whether to enable user-mode access for user-mode hardware loop CSRs.
0: Access is disabled
1: Access is enabled
(R/W)

STATE Configures state of the HWLP extension:
0x0: OFF (Accessing HWLP instructions/CSRs will trigger an illegal instruction exception)
0x1: INITIAL
0x2: CLEAN
0x3: DIRTY

Assuming state is not OFF, whenever HWLP CSRs are modified or HWLP instructions are executed the state will be updated to DIRTY. SW can set the state as INITIAL or CLEAN depending on the context. As specified in RISCV standard: When an extension's status is set to OFF, any instruction that attempts to read or write the corresponding state will cause an illegal instruction exception.
When the status is INITIAL, the corresponding state should have an initial constant value.
When the status is CLEAN, the corresponding state is potentially different from the initial value, but matches the last value stored on a context swap.
When the first iteration of HWLP is complete, the state changes to DIRTY. When the status is DIRTY, the corresponding state has potentially been modified since the last context save.
(R/W)
```