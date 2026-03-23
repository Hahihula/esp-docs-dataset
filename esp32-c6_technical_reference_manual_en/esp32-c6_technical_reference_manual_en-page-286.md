

```markdown
Register 7.25. GPIO_EXT_ETM_EVENT_CHn_CFG_REG (n: 0-7) (0x0060+0x4*n)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  | GPIO_EXT_ETM_CHn_EVENT_SEL    | Configures to select GPIO for ETM event channel.                            |
|     |                                | 0: Select GPIO0                                                              |
|     |                                | 1: Select GPIO1                                                              |
| ... |                                | ...                                                                         |
| 29  |                                | Select GPIO29                                                               |
| 30  |                                | Select GPIO30                                                               |
|     | (R/W)                          |                                                                             |
| 7   | GPIO_EXT_ETM_CHn_EVENT_EN     | Configures whether or not to enable ETM event send.                         |
|     |                                | 0: Not enable                                                                |
|     |                                | 1: Enable                                                                    |
|     | (R/W)                          |                                                                             |

GPIO_EXT_ETM_CHn_EVENT_SEL  Configures to select GPIO for ETM event channel.
0: Select GPIO0
1: Select GPIO1
......
29: Select GPIO29
30: Select GPIO30
(R/W)

GPIO_EXT_ETM_CHn_EVENT_EN   Configures whether or not to enable ETM event send.
0: Not enable
1: Enable
(R/W)
```