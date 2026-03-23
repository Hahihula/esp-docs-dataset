

```markdown
Register 26.39. UHCI_QUICK_SENT_REG (0x0030)

| Bit | Description |
|-----|-------------|
| 7   | UHCI_ALWAYS_SEND_EN<br>Set this bit to enable always_send mode to send short packets. (R/W) |
| 6   | UHCI_ALWAYS_SEND_NUM<br>This field is used to specify the always_send mode. (R/W) |
| 5-4 | reserved     |
| 3   | UHCI_SINGLE_SEND_EN<br>Set this bit to enable single_send mode to send short packets. (R/W/SC) |
| 2   | UHCI_SINGLE_SEND_NUM<br>This field is used to specify the single_send mode. (R/W) |
| 1-0 | reserved     |

UHCI_SINGLE_SEND_NUM This field is used to specify the single_send mode. (R/W)
UHCI_SINGLE_SEND_EN Set this bit to enable single_send mode to send short packets. (R/W/SC)

UHCI_ALWAYS_SEND_NUM This field is used to specify the always_send mode. (R/W)
UHCI_ALWAYS_SEND_EN Set this bit to enable always_send mode to send short packets. (R/W)
```

```markdown
Register 26.40. UHCI_REG_QO_WORD0_REG (0x0034)

| Bit | Description |
|-----|-------------|
| 31  | reserved     |
| 0   | UHCI_SEND_QO_WORD0<br>Reset: 0x000000 |

UHCI_SEND_QO_WORD0 This register is used as a quick_sent register when mode is specified by UHCI_ALWAYS_SEND_NUM or UHCI_SINGLE_SEND_NUM. (R/W)
```

```markdown
Register 26.41. UHCI_REG_QO_WORD1_REG (0x0038)

| Bit | Description |
|-----|-------------|
| 31  | reserved     |
| 0   | UHCI_SEND_QO_WORD1<br>Reset: 0x000000 |

UHCI_SEND_QO_WORD1 This register is used as a quick_sent register when mode is specified by UHCI_ALWAYS_SEND_NUM or UHCI_SINGLE_SEND_NUM. (R/W)
```