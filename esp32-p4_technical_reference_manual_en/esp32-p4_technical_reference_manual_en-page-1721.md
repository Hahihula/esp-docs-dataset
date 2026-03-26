
```markdown
Chapter 36 Image Signal Processor (ISP)

Register 36.101. ISP_AWB_BX_REG (0x0264)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 24  | ISP_AWB_X_BSIZE              |
| 23  |                              |
| ... | ...                          |
| 12  | ISP_AWB_X_START              |
| 11  |                              |
| 0   | Reset                        |

ISP_AWB_X_BSIZE Configures the AWB sub-window size in the X direction; minimum is 4. (R/W)
ISP_AWB_X_START Configures the AWB sub-window start coordinate in the X direction. (R/W)

Register 36.102. ISP_AWB_BY_REG (0x0268)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 24  | ISP_AWB_Y_BSIZE              |
| 23  |                              |
| ... | ...                          |
| 12  | ISP_AWB_Y_START              |
| 11  |                              |
| 0   | Reset                        |

ISP_AWB_Y_BSIZE Configures the AWB sub-window size in the Y direction. (R/W)
ISP_AWB_Y_START Configures the AWB sub-window start coordinate in the Y direction. (R/W)

Register 36.103. ISP_STATE_REG (0x026C)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| ... | ...                          |
| 2   | ISP_TAIL_BUSY                |
| 1   | ISP_HEADER_BUSY              |
| 0   | Reset                        |

ISP_TAIL_BUSY Represents whether isp_tail is busy.
    0: Idle
    1: Busy
    (RO)

ISP_HEADER_BUSY Represents whether isp_header is busy.
    0: Idle
    1: Busy
    (RO)
```