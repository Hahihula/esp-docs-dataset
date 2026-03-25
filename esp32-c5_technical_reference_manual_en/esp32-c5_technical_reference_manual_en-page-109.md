

```markdown
Register 2.84. dcsr (0x7B0)

| Bit | Field Name     | Description                                                                 |
|-----|----------------|-----------------------------------------------------------------------------|
| 31  | xdebugver      | Represents the debug version.<br>4: External debug support exists<br>(RO)   |
| 31  | reserved       |                                                                             |
| 28  | ebreakm        | When 1, ebreak instructions in Machine Mode enter debug mode.<br>(R/W)     |
| 27  | ebreaku        | When 1, ebreak instructions in User/Application Mode enter debug mode.<br>(R/W)|
| 16  | stepie         | Configures interrupt control in debug mode. O: Interrupts are disabled during single-stepping<br>1: Interrupts are enabled during single-stepping<br>(R/W)<br>Debugger must not change the value of this bit while the hart is running. |
| 15  | stopcount      | Configures mcycle counter control in debug mode. O: Increment counters as usual.<br>1: Not increment any counters while in debug mode or on ebreak instructions that cause entry into debug mode. These counters include the cycle and instret CSRs.<br>(R/W) |
| 14  | stoptime       | Configures timer control in debug mode.<br>O: Increment timers as usual.<br>1: Not increment any hart-local timers while in debug mode.<br>(R/W) |
| 13  | cause          | Explains why debug mode was entered. When there are multiple reasons to enter debug mode in a single cycle, the cause with the highest priority number is the one written.<br>1: An ebreak instruction was executed. (priority 3)<br>2: The Trigger Module caused a halt. (priority 4, highest)<br>3: haltreq was set. (priority 1)<br>4: The CPU core single-stepped because the step was set. (priority 0, lowest)<br>5: The hart halted directory out of reset due to resethalreq. (priority 2)<br>Other values are reserved for future use.<br>(RO) |
| 12  | mprven         | Configures whether to enable the functionality of MPRV bit in mstatus CSR during debug mode.<br>O: Disable<br>1: Enable<br>(R/W) |
| 11  | reserved       |                                                                             |
| 10  | step           |                                                                             |
| 9   | stopcount      |                                                                             |
| 8   | stoptime       |                                                                             |
| 7   | cause          |                                                                             |
| 6   | reserved       |                                                                             |
| 5   | mprven         |                                                                             |
| 4   | reserved       |                                                                             |
| 3   | step           |                                                                             |
| 2   | pv             |                                                                             |
| 1   | reserved       |                                                                             |
| 0   | Reset          |                                                                             |

Continued on the next page...
```