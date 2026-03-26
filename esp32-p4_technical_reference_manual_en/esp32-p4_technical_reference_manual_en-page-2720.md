

```markdown
Register 53.13. TWAI_ERR_CODE_CAP_REG (0x0030)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  |                                                                             |
| 8   | TWAI_ERR_CAPTURE_CODE_SEGMENT                                             |
| 7   | TWAI_ERR_CAPTURE_CODE_DIRECTION                                          |
| 6   | TWAI_ERR_CAPTURE_CODE_TYPE                                              |
| 5   |                                                                             |
| 4   |                                                                             |
| 3   |                                                                             |
| 2   |                                                                             |
| 1   |                                                                             |
| 0   | Reset                                                                      |

TWAI_ERR_CAPTURE_CODE_SEGMENT Represents the location of errors, see Table 53.4-11 for details. (RO)

TWAI_ERR_CAPTURE_CODE_DIRECTION Represents transmission direction of the node when an error occurs.
0: Error occurs when transmitting a message
1: Error occurs when receiving a message
(RO)

TWAI_ERR_CAPTURE_CODE_TYPE Represents error types.
0: Bit error
1: Form error
2: Stuff error
3: Others
(RO)

Register 53.14. TWAI_RX_ERR_CNT_REG (0x0038)

| Bit | Description |
|-----|-------------|
| 31  |             |
| 8   |             |
| 7   |             |
| 6   |             |
| 5   |             |
| 4   |             |
| 3   |             |
| 2   |             |
| 1   | TWAI_RX_ERR_CNT (R/W) |

TWAI_RX_ERR_CNT The RX error counter register, which reflects value changes in reception status. (R/W)
```