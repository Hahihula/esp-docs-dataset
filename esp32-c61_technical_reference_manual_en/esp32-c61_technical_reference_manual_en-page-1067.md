

```markdown
|bit|3|2|1|0|
|:----------|:----|:----|:----|:----|
|CMD_CLK|O|cap|tms|tdi|
|CMD_RST|1|O|O|srst|
|CMD_FLUSH| |O| | |
|CMD_RSV| | | | |
|CMD_REP| | |R1|RO|

## 29.3.4 USB-to-JTAG Interface: CMD_REP Usage Example

Here is a list of commands as an illustration of the usage of CMD_REP. Note that each command is a nibble, and in this example, the bytewise command stream would be 0xOD 0x5E 0xCF.

1. 0xO (CMD_CLK: cap=0, tdi=0, tms=0)
2. 0xD (CMD_REP: R1=O, RO=1)
3. 0x5 (CMD_CLK: cap=1, tdi=0, tms=1)
4. 0xE (CMD_REP: R1=1, RO=0)
5. 0xC (CMD_REP: R1=O, RO=O)
```