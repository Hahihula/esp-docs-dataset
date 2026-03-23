

```markdown
Register 1.35. dcsr (0x7B0)

| 31 | 28 | 27 | reserved | ebreakm | reserved | ebreaku | reserved | stopcount | stoptime | cause | reserved | step | prv |
|----:|----:|----:|----------|--------:|---------:|--------:|---------:|----------:|---------:|------:|---------:|-----:|-----:|
|    4|     0|     0|          0|        0|         0|        0|         0|          0|         0|      0|         0|     0|     0|

xdebugver Represents the debug version.
4: External debug support exists
(RO)

ebreakm When 1, ebreak instructions in Machine Mode enter Debug Mode. (R/W)

ebreaku When 1, ebreak instructions in User/Application Mode enter Debug Mode. (R/W)

stopcount This feature is not implemented. Debugger will always read this bit as 0. (RO)

stoptime This feature is not implemented. Debugger will always read this bit as 0. (RO)

cause Explains why Debug Mode was entered. When there are multiple reasons to enter Debug Mode in a single cycle, the cause with the highest priority number is the one written.
1: An ebreak instruction was executed. (priority 3)
2: The Trigger Module caused a halt. (priority 4)
3: haltreq was set. (priority 2)
4: The CPU core single stepped because step was set. (priority 1)
Other values are reserved for future use.
(RO)

step When set and not in Debug Mode, the core will only execute a single instruction and then enter Debug Mode.
If the instruction does not complete due to an exception, the core will immediately enter Debug Mode before executing the trap handler, with appropriate exception registers set.
Setting this bit does not mask interrupts. This is a deviation from the RISC-V External Debug Support Specification Version 0.13.
(R/W)

prv Contains the privilege level the core was operating in when Debug Mode was entered. A debugger can change this value to change the core's privilege level when exiting Debug Mode.
Only 0x3 (machine mode) and 0x0 (user mode) are supported. (R/W)
```