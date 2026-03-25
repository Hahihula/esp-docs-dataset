

```markdown
Chapter 1 ESP-RISC-V CPU
Register 1.22. mpcer (0x7E0)

INST_COMP Count Compressed Instructions. (R/W)
BRANCH_TAKEN Count Branches Taken. (R/W)
BRANCH Count Branches. (R/W)
JMP_UNCOND Count Unconditional Jumps. (R/W)
STORE Count Stores. (R/W)
LOAD Count Loads. (R/W)
IDLE Count IDLE Cycles. (R/W)
JMP_HAZARD Count Jump Hazards. (R/W)
LD_HAZARD Count Load Hazards. (R/W)
INST Count Instructions. (R/W)
CYCLE Count Clock Cycles. Cycle count does not increment during WFI mode.
Note: Each bit selects a specific event for counter to increment. If more than one event is selected and occurs simultaneously, then counter increments by one only.
(R/W)

Register 1.23. mpcmr (0x7E1)

COUNT_SAT Configures counter saturation.
O: Overflow on maximum value
1: Halt on maximum value
(R/W)

COUNT_EN Configures whether to enable the counter.
O: Disable
1: Enable
(R/W)
```