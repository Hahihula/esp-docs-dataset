

```markdown
|bit|3|2|1|0|
|:-----------|:----|:-----|:----|:----|
|CMD_CLK|0|cap|tms|tdi|
|CMD_RST|1|0|0|srst|
|CMD_FLUSH| | |1|0|
|CMD_RSV| | | | |
|CMD_REP| | |R1|RO|

```
#### 30.3.5 USB-to-JTAG Interface: CMD_REP usage example

Here is a list of commands as an illustration of the use of CMD_REP. Note each command is a nibble; in this example the bytewise command stream would be `0xOD 0x5E 0xCF`.
```