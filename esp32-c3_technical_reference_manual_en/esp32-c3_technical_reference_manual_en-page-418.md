

```markdown
## 15.5.2 How World Switch Log Registers are Updated

To explain this process, assuming:

1. At the beginning:
   - CPU is running in the Non-secure World;
   - Registers `WCL_CORE_O_STATUSTABLEn_REG(n: 0-31)` are all empty.

2. Then an interrupt occurs at Entry 9;

3. Then another interrupt with higher priority occurs at Entry 1;

4. Then the last interrupt with highest priority occurs at Entry 4.

The World Switch Log Table is updated as described below:

1. First, an interrupt occurs at Entry 9. At this time, CPU executes to the entry address of this interrupt. The World Switch Log Table is updated as described in Figure 15.5-2:

| entry | current | from_entry | from_world |
|-------|---------|------------|------------|
| 0     | 0       | 0          | 0          |
| 1     | 0       | 0          | 0          |
| 2     | 0       | 0          | 0          |
| 3     | 0       | 0          | 0          |
| 4     | 0       | 0          | 0          |
| 5     | 0       | 0          | 0          |
| 6     | 0       | 0          | 0          |
| 7     | 0       | 0          | 0          |
| 8     | 0       | 0          | 0          |
| **9** | **1**   | **32**     | **1**      |
| ...   | 0       | 0          | 0          |
| 30     | 0       | 0          | 0          |
| 31     | 0       | 0          | 0          |

Figure 15.5-2. Nested Interrupts Handling - Entry 9

At this time:

* `WCL_CORE_O_STATUSTABLE9_REG`
    - Field `WCL_CORE_O_FROM_WORLD_9` is updated to 1, indicating CPU was in Non-secure World before the interrupt;
    - Field `WCL_CORE_O_FROM_ENTRY_9` is updated to 32, indicating there was not any interrupt before this one;
    - Field `WCL_CORE_O_CURRENT_9` is updated to 1, indicating the CPU is currently at the interrupt monitored at Entry 9.
* Other `WCL_CORE_O_STATUSTABLEn_REG` registers are not updated.

2. Then another interrupt with higher priority occurs at Entry 1. At this time, CPU executes to the entry address of this interrupt. The World Switch Log Table is updated again as described in Figure 15.5-3:
```