

```markdown
Register 6.28. GPIO_EXT_PAD_COMP_FILTER_O_REG (0x005C)

GPIO_EXT_ZERO_DET_FILTER_CNT_O   Configures the period of masking new interrupt source for Analog Voltage Comparator.
Measurement unit: HP IO MUX operating clock cycle
(R/W)
```

```markdown
Register 6.29. GPIO_EXT_ETM_EVENT_CHn_CFG_REG (n: 0-7) (0x0118+0x4*n)

GPIO_EXT_ETM_CHn_EVENT_SEL   Configures to select GPIO for ETM event channel.
0: Select GPIO0
1: Select GPIO1
......
28: Select GPIO28
29: Select GPIO29
30~31: Reserved
(R/W)

GPIO_EXT_ETM_CHn_EVENT_EN   Configures whether or not to enable ETM event send.
0: Not enable
1: Enable
(R/W)
```