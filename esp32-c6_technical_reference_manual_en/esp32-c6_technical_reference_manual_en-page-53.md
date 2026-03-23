

```markdown
Register 1.22. mpcer (0x7E0)

| Bit | Field Name         | Description                                                                 |
|-----|--------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)         |                                                                             |
| 11  | INST_COMP          | Count Compressed Instructions. (R/W)                                       |
| 10  | BRANCH_TAKEN       | Count Branches Taken. (R/W)                                                |
| 9   | BRANCH             | Count Branches. (R/W)                                                       |
| 8   | JMP_UNCOND         | Count Unconditional Jumps. (R/W)                                            |
| 7   | STORE              | Count Stores. (R/W)                                                         |
| 6   | LOAD               | Count Loads. (R/W)                                                          |
| 5   | IDLE               | Count IDLE Cycles. (R/W)                                                    |
| 4   | JMP_HAZARD         | Count Jump Hazards. (R/W)                                                   |
| 3   | LD_HAZARD          | Count Load Hazards. (R/W)                                                   |
| 2   | INST               | Count Instructions. (R/W)                                                   |
| 1   | CYCLE              | Count Clock Cycles. Cycle count does not increment during WFI mode.<br>Note: Each bit selects a specific event for counter to increment. If more than one event is selected and occurs simultaneously, then counter increments by one only.<br>(R/W) |

Register 1.23. mpcmr (0x7E1)

| Bit | Field Name   | Description                                                                 |
|-----|--------------|-----------------------------------------------------------------------------|
| 31  | (reserved)   |                                                                             |
| 2   | COUNT_SAT    | Configures counter saturation.<br>0: Overflow on maximum value<br>1: Halt on maximum value<br>(R/W) |
| 1   | COUNT_EN     | Configures whether to enable the counter.<br>0: Disable<br>1: Enable<br>(R/W)      |

Espressif Systems
53
ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```