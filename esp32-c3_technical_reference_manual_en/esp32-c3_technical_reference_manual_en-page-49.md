
```markdown
Register 1.18. dcsr (0x7B0)

| Bit | Field Name     | Description                                                                 |
|-----|----------------|-----------------------------------------------------------------------------|
| 31  | xdebugver      | Debug version. (RO)<br>• 4: External debug support exists                   |
| 28  | reserved       |                                                                             |
| 27  |                |                                                                             |
| 16  | ebreakm        | When 1, ebreak instructions in Machine Mode enter Debug Mode. (R/W)         |
| 15  | ebreaku        | When 1, ebreak instructions in User/Application Mode enter Debug Mode. (R/W)|
| 14  | stopcount      | This bit is not implemented. Debugger will always read this bit as 0. (RO)   |
| 13  | stoptime       | This feature is not implemented. Debugger will always read this bit as 0. (RO)|
| 12  | cause          | Explains why Debug Mode was entered.<br>When there are multiple reasons to enter Debug Mode in a single cycle, the cause with the highest priority number is the one written:<br>1. An ebreak instruction was executed. (priority 3)<br>2. The Trigger Module caused a halt. (priority 4)<br>3. halreq was set. (priority 2)<br>4. The CPU core single stepped because step was set. (priority 1)<br>Other values are reserved for future use. (RO) |
| 11  |                |                                                                             |
| 10  | reserved       |                                                                             |
| 9   | stopcount      |                                                                             |
| 8   | stoptime       |                                                                             |
| 7   | cause          |                                                                             |
| 6   | reserved       |                                                                             |
| 5   | step           | When set and not in Debug Mode, the core will only execute a single instruction and then enter Debug Mode. Interrupts are enabled* when this bit is set.<br>If the instruction does not complete due to an exception, the core will immediately enter Debug Mode before executing the trap handler, with appropriate exception registers set. (R/W) |
| 4   | reserved       |                                                                             |
| 3   | prv             | Contains the privilege level the core was operating in when Debug Mode was entered.<br>A debugger can change this value to change the core’s privilege level when exiting Debug Mode.<br>Only 0x3 (machine mode) and 0x0 (user mode) are supported. |
| 2   |                |                                                                             |
| 1   |                |                                                                             |
| 0   | Reset          |                                                                             |

*Note: Different from RISC-V Debug specification 0.13

Register 1.19. dpc (0x7B1)

| Bit | Field Name | Description                                                                 |
|-----|------------|-----------------------------------------------------------------------------|
| 31  |            |                                                                             |
|     |            |                                                                             |
| 0   | Reset      |                                                                             |

dpc Upon entry to debug mode, dpc is written with the virtual address of the instruction that encountered the exception. When resuming, the CPU core’s PC is updated to the virtual address stored in dpc. A debugger may write dpc to change where the CPU resumes. (R/W)
```