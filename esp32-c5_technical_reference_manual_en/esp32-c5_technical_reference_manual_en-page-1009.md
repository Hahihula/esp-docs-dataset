

```markdown
| Name                     | Description                                                                 | Address   | Access |
|--------------------------|-----------------------------------------------------------------------------|-----------|--------|
| Clock Gate Register      |                                                                             |           |        |
| HUK_CLK_REG              | Clock gate control register                                                 | 0x0004    | R/W    |

| Interrupt Registers      |                                                                             |           |        |
|--------------------------|                                                                             |           |        |
| HUK_INT_RAW_REG          | Interrupt raw register (valid in level)                                    | 0x0008    | RO/WTG/SS |
| HUK_INT_ST_REG           | Interrupt status register                                                   | 0x000C    | RO     |
| HUK_INT_ENA_REG          | Interrupt enable register                                                   | 0x0010    | R/W    |
| HUK_INT_CLR_REG          | Interrupt clear register                                                    | 0x0014    | WT     |

| Configuration Register   |                                                                             |           |        |
|--------------------------|                                                                             |           |        |
| HUK_CONF_REG             | Configuration register                                                      | 0x0020    | R/W    |

| Control Register         |                                                                             |           |        |
|--------------------------|                                                                             |           |        |
| HUK_START_REG            | Control register                                                            | 0x0024    | WT     |

| State Register           |                                                                             |           |        |
|--------------------------|                                                                             |           |        |
| HUK_STATE_REG            | HUK Generator state register                                                | 0x0028    | RO     |

| Result Register          |                                                                             |           |        |
|--------------------------|                                                                             |           |        |
| HUK_STATUS_REG           | HUK status register                                                         | 0x0034    | RO     |

| Version Register         |                                                                             |           |        |
|--------------------------|                                                                             |           |        |
| HUK_DATE_REG             | Version control register                                                    | 0x00FC    | R/W    |
```

```markdown
| Name                     | Description                                                                 | Address   | Access |
|--------------------------|-----------------------------------------------------------------------------|-----------|--------|
| Clock Gate Register      |                                                                             |           |        |
| KEYMNG_CLK_REG           | Clock gate control register                                                 | 0x0004    | R/W    |

| Interrupt Registers      |                                                                             |           |        |
|--------------------------|                                                                             |           |        |
| KEYMNG_INT_RAW_REG       | Interrupt raw register (valid in level)                                    | 0x0008    | RO/WTG/SS |
| KEYMNG_INT_ST_REG        | Interrupt status register                                                   | 0x000C    | RO     |
| KEYMNG_INT_ENA_REG       | Interrupt enable register                                                   | 0x0010    | R/W    |
| KEYMNG_INT_CLR_REG       | Interrupt clear register                                                    | 0x0014    | WT     |

| Static Configuration Registers |                                                                             |           |        |
|-------------------------------|                                                                             |           |        |
| KEYMNG_STATIC_REG            | Static configuration register                                                | 0x0018    | R/W    |
| KEYMNG_LOCK_REG              | Static configuration lock register                                          | 0x001C    | R/W1   |

| Configuration register       |                                                                             |           |        |
|------------------------------|                                                                             |           |        |
| KEYMNG_CONF_REG              | Configuration register                                                      | 0x0020    | R/W    |
```