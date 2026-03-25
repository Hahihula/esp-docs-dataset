
```markdown
| bit | 3   | 2 | 1 | 0 |
|-----|-----|---|---|---|
| CMD_CLK | 0 | cap | tms | tdi |
| CMD_RST | 1 | 0 | 0 | srst |
| CMD_FLUSH | 1 | 0 | 1 | 0 |
| CMD_RSV | 1 | 0 | 1 | 1 |
| CMD_REP | 1 | 1 | R1 | RO |

*   `CMD_CLK` will set the TDI and TMS as the indicated values and emit one clock pulse on TCK. If the CAP bit is 1, it will instruct the JTAG response capture unit to capture the state of the TDO line. This instruction forms the basis of JTAG communication.
*   `CMD_RST` will set the state of the SRST line as the indicated value. This can be used to reset ESP32-H2.
*   `CMD_FLUSH` will instruct the JTAG response capture unit to flush the buffer of all bits it collected so the host is able to read them. Note that in some cases, a JTAG transaction will end in an odd number of commands and as such an odd number of nibbles. In this case, it is allowed to repeat the `CMD_FLUSH` command to get an even number of nibbles fitting an integer number of bytes.
*   `CMD_RSV` is reserved in the current implementation. This command will be ignored when received by ESP32-H2.
*   `CMD_REP` repeats the last (non-CMD_REP) command for a certain number of times. The purpose is to compress command streams which repeat the CMD_CLK instruction for multiple times. A command such as `CMD_CLK` can be followed by multiple `CMD_REP` commands. The number of repetitions done by one `CMD_REP` can be expressed as repetition_count = (R1 × 2 + R0) × (4^cmd_rep_count), where cmd_rep_count indicates the number of the CMD_REP instruction that went directly before it. A CMD_REP instruction can be repeated up to five times, for a maximum of 1023 repeats of the initial instruction. Note that the CMD_REP command is only intended to repeat a CMD_CLK command. Specifically, using it on a `CMD_FLUSH` command may lead to an unresponsive USB device, and a USB reset will be required to recover it.

### 33.3.4 USB-to-JTAG Interface: CMD_REP Usage Example

Here is a list of commands as an illustration of the usage of CMD_REP. Note that each command is a nibble, and in this example, the bytewise command stream would be `0x0D` `0x5E` `0xCF`.

1.  `0x0` (`CMD_CLK`: cap=0, tdi=0, tms=0)
2.  `0xD` (`CMD_REP`: R1=0, RO=1)
3.  `0x5` (`CMD_CLK`: cap=1, tdi=0, tms=1)
4.  `0xE` (`CMD_REP`: R1=1, RO=0)
5.  `0xC` (`CMD_REP`: R1=0, RO=0)
6.  `0xF` (`CMD_REP`: R1=1, RO=1)

The following shows what happens at every step:

1.  TCK is clocked with the TDI and TMS lines set to 0. No data is captured.
```