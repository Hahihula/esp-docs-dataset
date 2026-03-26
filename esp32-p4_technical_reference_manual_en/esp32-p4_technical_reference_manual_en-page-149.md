

```markdown
Register 1.120. dcsr (0x7B0)

| Bit | Field Name     | Description                                                                 |
|-----|----------------|-----------------------------------------------------------------------------|
| 31  | xdebugver      | Represents the debug version.<br>4: External debug support exists<br>(RO)   |
| 31  | reserved       |                                                                             |
| 28  |                |                                                                             |
| 27  |                |                                                                             |
| 16  | ebreakm         | When 1, ebreak instructions in Machine Mode enter debug mode.<br>(R/W)     |
| 15  | ebreaku         | When 1, ebreak instructions in User/Application Mode enter debug mode.<br>(R/W)|
| 14  | reserved        |                                                                             |
| 13  | stepie          | Configures interrupt control in debug mode. O: Interrupts are disabled during single-stepping<br>1: Interrupts are enabled during single-stepping<br>(R/W)<br>Debugger must not change the value of this bit while the hart is running. |
| 12  | stopcount       | Configures mcycle counter control in debug mode. O: Increment counters as usual.<br>1: Not increment any counters while in debug mode or on ebreak instructions that cause entry into debug mode. These counters include the cycle and instret CSRs.<br>(R/W) |
| 11  |                |                                                                             |
| 10  | stoptime        | Configures timer control in debug mode.<br>O: Increment timers as usual.<br>1: Not increment any hart-local timers while in debug mode.<br>(R/W)   |
| 9   | cause           | Explains why debug mode was entered. When there are multiple reasons to enter debug mode in a single cycle, the cause with the highest priority number is the one written.<br>1: An ebreak instruction was executed. (priority 3)<br>2: The Trigger Module caused a halt. (priority 4, highest)<br>3: haltreq was set. (priority 1)<br>4: The CPU core single-stepped because the step was set. (priority 0, lowest)<br>5: The hart halted directory out of reset due to resethalreq. (priority 2)<br>Other values are reserved for future use.<br>(RO) |
| 8   | mprven          | Configures whether to enable the functionality of MPRV bit in mstatus CSR during debug mode.<br>O: Disable<br>1: Enable<br>(R/W) |
| 7   | reserved        |                                                                             |
| 6   | step            |                                                                             |
| 5   | reserved        |                                                                             |
| 4   |                |                                                                             |
| 3   | pv              |                                                                             |
| 2   |                |                                                                             |
| 1   |                |                                                                             |
| 0   | Reset           |                                                                             |

Continued on the next page...
```