

```markdown
Register 4.18. dcsr (0x7B0)

| Bit | Field Name     | Description                                                                 |
|-----|----------------|-----------------------------------------------------------------------------|
| 31  | xdebugver      | Represents the debug version.<br>4: External debug support exists<br>(RO)   |
| 28-27|               | (reserved)                                                                  |
| 16  | ebreakm        | Configures execution of the EBREAK instruction in machine mode.<br>0: Trigger an exception with mcause = 3<br>1: Enter debug mode<br>(R/W) |
| 15  | ebreakm_n      | (reserved)                                                                  |
| 14  |               | (reserved)                                                                  |
| 13  | ebreaku        | Configures execution of the EBREAK instruction in user mode.<br>0: Trigger an exception with mcause = 3 as described in privileged mode<br>1: Enter debug mode<br>(R/W) |
| 12  |               | (reserved)                                                                  |
| 11  | ebreaku_n      | (reserved)                                                                  |
| 9   |               | (reserved)                                                                  |
| 8   | cause          | Represents the reason why debug mode was entered. When there are multiple reasons to enter debug mode in a single cycle, the cause with the highest priority number is the one written.<br>1: An EBREAK instruction was executed. (priority 3)<br>2: The Trigger Module caused a halt. (priority 4)<br>3: haltreq was set. (priority 2)<br>4: The CPU core single stepped because step was set. (priority 1)<br>Other values: Reserved for future use<br>(RO) |
| 7   |               | (reserved)                                                                  |
| 6   |               | (reserved)                                                                  |
| 5   |               | (reserved)                                                                  |
| 4   |               | (reserved)                                                                  |
| 3   | step           | When set and not in Debug Mode, the core will only execute a single instruction and then enter Debug Mode.<br>If the instruction does not complete due to an exception, the core will immediately enter Debug Mode before executing the trap handler, with appropriate exception registers set.<br>Setting this bit does not mask interrupts. This is a deviation from the RISC-V External Debug Support Specification Version 0.13.<br>(R/W) |
| 2   |               | (reserved)                                                                  |
| 1   | prv            | Contains the privilege level the core is operating in when debug mode is entered. A debugger can change this value to change the core’s privilege level when exiting debug mode. Only 0x3 (machine mode) and 0x0 (user mode) are supported.<br>(RO) |
| 0   | Reset          |                                                                             |
```