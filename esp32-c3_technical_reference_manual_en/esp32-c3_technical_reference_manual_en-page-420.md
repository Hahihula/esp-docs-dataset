

```markdown
- Field `WCL_CORE_O_FROM_WORLD_4` is updated to 0, indicating the CPU was in Secure World before this interrupt.
- Field `WCL_CORE_O_FROM_ENTRY_4` is updated to 1, indicating the CPU was the interrupt at Entry 1.
- Field `WCL_CORE_O_CURRENT_4` is updated to 1, indicating the CPU is currently at the interrupt monitored an Entry 4.

• `WCL_CORE_O_STATUSTABLE1_REG`
    - Field `WCL_CORE_O_CURRENT_1` is updated to 0, indicating the CPU is no longer at the interrupt monitored at Entry 1 (Instead CPU is at the interrupt monitored at Entry 4 already).
    - Fields `WCL_CORE_O_FROM_WORLD_1` and `WCL_CORE_O_FROM_ENTRY_1` are not updated.
• Other `WCL_CORE_O_STATUSTABLEn_REG` registers are not updated.

### 15.5.3 How to Read World Switch Log Registers

By reading World Switch Log Registers, we get to understand the information of previous world switches and nested interrupts, thus being able to restore to previous world.

Steps are described below: (See Figure 15.5-4 as an example):

1. Read Register `WCL_CORE_O_STATUSTABLE_CURRENT_REG`, and understand CPU is now at the interrupt monitored at Entry 4.
2. Read 1 from Field `WCL_CORE_O_FROM_ENTRY_4`, and understand the CPU was at an interrupt monitored at Entry 1.
3. Read 9 from Field `WCL_CORE_O_FROM_ENTRY_1`, and understand the CPU was at an interrupt monitored at Entry 9.
4. Read 32 from `WCL_CORE_O_FROM_ENTRY_9`, and understand CPU wasn’t at any interrupt. Then read 1 from `WCL_CORE_O_FROM_WORLD_9`, and understand CPU was in Non-secure World at the beginning.

### 15.5.4 Nested Interrupts

To support interrupt nesting, World controller provides additional configuration to update **World Switch Log**.
See details in Section Programming Procedure below.

#### 15.5.4.1 Programming Procedure

Handling the interrupt at Entry A:

1. Save context.
2. Configure `WCL_CORE_O_MSTATUS_MIE_REG` register to enable updating the World Switch Log table.

    - After entering the interrupt and exception vector, CPU will automatically turn off the global interrupt enable to avoid interrupt nesting. After saving the context, the global interrupt enable can be turned on again to respond to higher-level interrupts.
    - The World Controller `WCL_CORE_O_MSTATUS_MIE_REG` register also supports a similar feature of global interrupt enable. When any entry trigger is detected, `WCL_CORE_O_MSTATUS_MIE_REG` will
```