

```markdown
Chapter 3 Low-Power CPU

Register 3.18. dcsr (0x7B0)

xdebugver Represents the debug version.
4: External debug support exists
(RO)

ebreakm Configures execution of the EBREAK instruction in machine mode.
0: Trigger an exception with mcause = 3
1: Enter debug mode
(R/W)

ebreaku Configures execution of the EBREAK instruction in user mode.
0: Trigger an exception with mcause = 3 as described in privileged mode
1: Enter debug mode
(R/W)

cause Represents the reason why debug mode was entered. When there are multiple reasons to enter debug mode in a single cycle, the cause with the highest priority number is the one written.
1: An EBREAK instruction was executed. (priority 3)
2: The Trigger Module caused a halt. (priority 4)
3: haltreq was set. (priority 2)
4: The CPU core single stepped because step was set. (priority 1)
Other values: reserved for future use
(RO)

step When set and not in Debug Mode, the core will only execute a single instruction and then enter Debug Mode.
If the instruction does not complete due to an exception, the core will immediately enter Debug Mode before executing the trap handler, with appropriate exception registers set.
Setting this bit does not mask interrupts. This is a deviation from the RISC-V External Debug Support Specification Version 0.13.
(R/W)

prv Contains the privilege level the core is operating in when debug mode is entered. A debugger can change this value to change the core's privilege level when exiting debug mode. Only 0x3 (machine mode) and 0x0 (user mode) are supported. (RO)
```