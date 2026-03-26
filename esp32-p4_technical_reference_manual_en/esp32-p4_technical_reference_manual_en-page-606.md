

```markdown
Register 9.48. GPIO_EXT_ETM_EVENT_CHn_CFG_REG (n: 0 - 7) (0x0060+0x4*n)

31                                 8                 7     6     5                     0
+-------------------------------------------------------------------------------------------------+
| RESERVED | RESERVED | RESERVED | RESERVED | RESERVED | RESERVED | RESERVED |
+-------------------------------------------------------------------------------------------------+

GPIO_EXT_ETM_CHn_EVENT_SEL   Configures to select GPIO for ETM event channel.
    0: Select GPIO0
    1: Select GPIO1
    ...
    53: Select GPIO53
    54: Select GPIO54
    (R/W)

GPIO_EXT_ETM_CHn_EVENT_EN     Configures whether or not to enable ETM event send.
    0: Not enable
    1: Enable
    (R/W)
```