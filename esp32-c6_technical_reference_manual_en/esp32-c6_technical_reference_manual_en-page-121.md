

```markdown
Register 3.19. dpc (0x7B1)

dpc Upon entry to debug mode, dpc is written with the address of the next instruction that will be executed. When resuming, the CPU core's PC is updated to the address stored in dpc. In debug mode, dpc can be modified. This field can be accessed in debug mode. (R/W)

Register 3.20. dscratch0 (0x7B2)

dscratch0 Used by the debug module internally. (R/W)

Register 3.21. dscratch1 (0x7B3)

dscratch1 Used by the debug module internally.(R/W)
```

## 3.5 Hardware Trigger

### 3.5.1 Features

Hardware Trigger module provides breakpoint and watchpoint capability for debugging. It has the following features:

* Two independent trigger units
* Configurable unit to match the address of the program counter
* Able to halt execution and transfer control to the debugger

### 3.5.2 Functional Description

The hardware trigger module provides three CSRs. See Section 3.5 for details. Among these, tdata1 and tdata2 are abstract CSRs, which means they are shadow registers for accessing internal registers in the trigger units, one at a time.
```