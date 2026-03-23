

```markdown
2. Configure Register WCL_CORE_O_ENTRY_CHECK_REG to enable the monitoring of one or more certain entries (0: disable; 1: enable).

- Bit 0 controls the entry monitoring of exception
- Bit x controls the entry monitoring of interrupt Entry x (x = 1~31), respectively

Note that, once configured, register WCL_CORE_O_ENTRY_CHECK_REG is always effective till it’s disabled again, meaning you don’t need to configure this register every time after each world switch.

3. Configure WCL_CORE_O_MSTATUS_MIE_REG to enable updating the World Switch Log. Otherwise, this log will not be updated for world switches. For detailed information about the World Switch Log, see Section 15.5.
```

## 15.5 World Switch Log

In actual use cases, CPU is switching between two worlds quite frequently and has to deal with nested interrupts. To be able to restore to the previous world, World Controller keeps a world switching log in a series of registers, which is called "World Switch Log Table".

### 15.5.1 Structure of World Switch Log Register

ESP32-C3’s World Switch Log Table consists of 32 WCL_CORE_O_STATUSTABLEn_REG(n: 0-31) registers (see Figure 15.5-1). The Entry x, is logged in WCL_CORE_O_STATUSTABLEx_REG.

![Figure 15.5-1. World Switch Log Register](image-placeholder)

```markdown
StatusTableX

7    6          1     0
current   from_world_entry   from_world

WCL_CORE_O_FROM_WORLD_n: logs the world information before the world switch.
- 0: CPU was in Secure World
- 1: CPU was in Non-secure World

WCL_CORE_O_FROM_ENTRY_n: logs the entry information before the world switch, in total of 6 bits.
- 0~31: CPU is currently jumping from another interrupt/exception entry 0~31
- 32: CPU was not at any interrupts monitored at any entry

WCL_CORE_O_CURRENT_n: indicates if CPU is at the interrupt monitored at the current entry. When CPU is at the interrupt monitored at Entry x,
- WCL_CORE_O_CURRENT_x is updated to 1;
- and the same field of all other entries are updated to 0.
```