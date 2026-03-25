

```markdown
| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 24 | 23 | 22 | 21 | 20 | 18 | 17 | 16 | 15 | 14 | 12 | 11 | 10 | 9 | 8 | 6 | 5 | 4 | 3 | 2 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  |    | 0x0| 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0x0| 0  | 0  | 0  | 0  | 0  | 0  | 0x0| Reset|
```

**Register 6.32. GPIO_EXT_ETM_TASK_P2_CFG_REG (0x0160)**

`GPIO_EXT_ETM_TASK_GPIO10_SEL` Configures to select an ETM task channel for GPIO10.
- 0: Select channel 0
- 1: Select channel 1
```
```

```
```

7: Select channel 7  
(R/W)

`GPIO_EXT_ETM_TASK_GPIO10_EN` Configures whether or not to enable GPIO10 to response ETM task.
- 0: Not enable
- 1: Enable  
(R/W)

`GPIO_EXT_ETM_TASK_GPIO11_SEL` Configures to select an ETM task channel for GPIO11.
- 0: Select channel 0
- 1: Select channel 1
```
```

```
```

7: Select channel 7  
(R/W)

`GPIO_EXT_ETM_TASK_GPIO11_EN` Configures whether or not to enable GPIO11 to response ETM task.
- 0: Not enable
- 1: Enable  
(R/W)

`GPIO_EXT_ETM_TASK_GPIO12_SEL` Configures to select an ETM task channel for GPIO12.
- 0: Select channel 0
- 1: Select channel 1
```
```

```
```

7: Select channel 7  
(R/W)

`GPIO_EXT_ETM_TASK_GPIO12_EN` Configures whether or not to enable GPIO12 to response ETM task.
- 0: Not enable
- 1: Enable  
(R/W)
```