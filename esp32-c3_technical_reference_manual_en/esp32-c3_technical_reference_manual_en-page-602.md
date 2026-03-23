

```markdown
Register 26.58. UHCI_PKT_THRES_REG (0x007C)
```

| Reset | 31                                 13   12                         0 |
|-------|------------------------------------|--------------------------|------------------------|
|       |                                    |                          | `UHCI_PKT_THRS`        |
|       |                                    |                          |                        |
|       |                                    |                          | `0x80`                 |
| Reset |                                    |                          |

**UHCI_PKT_THRS** This field is used to configure the maximum value of the packet length when UHCI_HEAD_EN is 0. (R/W)
```