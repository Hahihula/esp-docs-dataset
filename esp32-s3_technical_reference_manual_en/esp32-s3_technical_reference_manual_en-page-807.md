**Chapter Title:**
Chapter 16 World Controller (WCL)

**Body Text:**

The World Switch Log Table is updated as described below:

1. First, an interrupt occurs at Entry 9. At this time, CPU executes to the entry address of this interrupt. The World Switch Log Table is updated as described in Figure **16.5-2**.

**Figure Caption (1):**
Figure 16.5-2. Nested Interrupts Handling - Entry 9

| entry | current | from_entry | from_world |
|-------|--------|------------|-----------|
| 0     | 0      | 0          | 0         |
| 1     | 0      | 0          | 0         |
| ...   | ...    | ...        | ...       |

- Field `WCL_CORE_m_FROM_WORLD_9` is updated to 1, indicating CPU was in Non-secure World before the interrupt.
- Field `WCL_CORE_m ENTRY_9` is updated to 0, indicating there was not any interrupt before this one.
- Field `WCL_CORE_m_CURRENT_9` is updated to 1, indicating the CPU is currently at the interrupt monitored at Entry 9.

Other WCL_CORE_m_STATUSABLE_n_registers are not updated.

2. Then another interrupt with higher priority occurs at Entry 1. At this time, CPU executes to the entry address of this interrupt. The World Switch Log Table is updated again as described in Figure **16.5-3**:

**Figure Caption (2):**
Figure 16.5-3. Nested Interrupts Handling - Entry 1

| entry | current | from_entry | from_world |
|-------|--------|------------|-----------|
| 0     | 0      | 0          | 0         |
| 1     | 9      | 0          | 0         |
| ...   | ...    | ...        | ...       |

- Field `WCL_CORE_m_FROM_WORLD_1` is updated to 0, indicating the CPU was in Secure World before this interrupt.
- Field `WCL_CORE_m ENTRY_1` is updated to 9, indicating the CPU was executing the interrupt at Entry 9.

**Footer:**
Espressif Systems
807 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback