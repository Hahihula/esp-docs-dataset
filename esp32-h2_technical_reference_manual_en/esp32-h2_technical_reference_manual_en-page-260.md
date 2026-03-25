

```markdown
Register 6.27. GPIO_EXT_ETM_EVENT_CHn_CFG_REG (n: 0-7) (0x0060+0x4*n)

| Bit | Field Name                          | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 30  | GPIO_EXT_ETM_CHn_EVENT_SEL          | Configures to select GPIO for ETM event channel.                            |
|     |                                      | 0: Select GPIO0                                                              |
|     |                                      | 1: Select GPIO1                                                              |
| ... |                                      | ...                                                                          |
| 26  |                                      | Select GPIO26                                                               |
| 27  |                                      | Select GPIO27                                                               |
| R/W |                                      | (R/W)                                                                        |

GPIO_EXT_ETM_CHn_EVENT_EN Configures whether or not to enable ETM event send.
0: Not enable
1: Enable
(R/W)
```