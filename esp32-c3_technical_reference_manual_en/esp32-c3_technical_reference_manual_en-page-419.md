

```markdown
| entry | current | from_entry | from_world |
|-------|---------|------------|------------|
| 0     | 0       | 0          | 0          |
| 1     | 1       | 9          | 0          |
| 2     | 0       | 0          | 0          |
| 3     | 0       | 0          | 0          |
| 4     | 0       | 0          | 0          |
| 5     | 0       | 0          | 0          |
| 6     | 0       | 0          | 0          |
| 7     | 0       | 0          | 0          |
| 8     | 0       | 0          | 0          |
| 9     | 0       | 32         | 1          |
| ...   |          |            |            |
| 30    |          |            |            |
| 31    |          |            |            |

Figure 15.5-3. Nested Interrupts Handling - Entry 1

At this time:

* WCL_CORE_O_STATUSTABLE1_REG
  - Field WCL_CORE_O_FROM_WORLD_1 is updated to 0, indicating the CPU was in Secure World before this interrupt.
  - Field WCL_CORE_O_FROM_ENTRY_1 is updated to 9, indicating the CPU was executing the interrupt at Entry 9.
  - Field WCL_CORE_O_CURRENT_1 is updated to 1, indicating CPU is currently at the interrupt monitored at Entry 1.

* WCL_CORE_O_STATUSTABLE9_REG
  - Field WCL_CORE_O_CURRENT_9 is updated to 0, indicating CPU is no longer at the interrupt monitored at Entry 9 (Instead, CPU is at the interrupt monitored at Entry 1 already).
  - Fields WCL_CORE_O_FROM_WORLD_9 and WCL_CORE_O_FROM_ENTRY_9 stay the same.

* Other WCL_CORE_O_STATUSTABLEn_REG registers are not updated.

3. Then the last interrupt with highest priority occurs at Entry 4. At this time, CPU executes to the entry address of interrupt 4. The World Switch Log Table is updated again as described in Figure 15.5-4:

| entry | current | from_entry | from_world |
|-------|---------|------------|------------|
| 0     | 0       | 0          | 0          |
| 1     | 0       | 9          | 0          |
| 2     | 0       | 0          | 0          |
| 3     | 0       | 0          | 0          |
| 4     | 1       | 1          | 0          |
| 5     | 0       | 0          | 0          |
| 6     | 0       | 0          | 0          |
| 7     | 0       | 0          | 0          |
| 8     | 0       | 0          | 0          |
| 9     | 0       | 32         | 1          |
| ...   |          |            |            |
| 30    |          |            |            |
| 31    |          |            |            |

Figure 15.5-4. Nested Interrupts Handling - Entry 4

At this time:

* WCL_CORE_O_STATUSTABLE4_REG
```