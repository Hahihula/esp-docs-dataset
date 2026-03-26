

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| Clock Control Register                    |                                                                             |           |        |
| SYSTIMER_CONF_REG                          | Configure system timer clock                                               | 0x0000    | R/W    |
| UNIT0 Control and Configuration Registers  |                                                                             |           |        |
| SYSTIMER_UNITO_OP_REG                      | Read UNITO value to registers                                              | 0x0004    | varies |
| SYSTIMER_UNITO_LOAD_HI_REG                 | High 20 bits to be loaded to UNITO                                         | 0x000C    | R/W    |
| SYSTIMER_UNITO_LOAD_LO_REG                 | Low 32 bits to be loaded to UNITO                                           | 0x0010    | R/W    |
| SYSTIMER_UNITO_VALUE_HI_REG                | UNITO value, high 20 bits                                                   | 0x0040    | RO     |
| SYSTIMER_UNITO_VALUE_LO_REG                | UNITO value, low 32 bits                                                    | 0x0044    | RO     |
| SYSTIMER_UNITO_LOAD_REG                    | UNITO synchronization register                                              | 0x005C    | WT     |
| UNIT1 Control and Configuration Registers   |                                                                             |           |        |
| SYSTIMER_UNIT1_OP_REG                      | Read UNIT1 value to registers                                               | 0x0008    | varies |
| SYSTIMER_UNIT1_LOAD_HI_REG                 | High 20 bits to be loaded to UNIT1                                         | 0x0014    | R/W    |
| SYSTIMER_UNIT1_LOAD_LO_REG                 | Low 32 bits to be loaded to UNIT1                                           | 0x0018    | R/W    |
| SYSTIMER_UNIT1_VALUE_HI_REG                | UNIT1 value, high 20 bits                                                   | 0x0048    | RO     |
| SYSTIMER_UNIT1_VALUE_LO_REG                | UNIT1 value, low 32 bits                                                    | 0x004C    | RO     |
| SYSTIMER_UNIT1_LOAD_REG                    | UNIT1 synchronization register                                              | 0x0060    | WT     |
| Comparator0 Control and Configuration Registers |                                                                             |           |        |
| SYSTIMER_TARGETO_HI_REG                    | Alarm value to be loaded to COMPO, high 20 bits                             | 0x001C    | R/W    |
| SYSTIMER_TARGETO_LO_REG                     | Alarm value to be loaded to COMPO, low 32 bits                              | 0x0020    | R/W    |
| SYSTIMER_TARGETO_CONF_REG                   | Configure COMPO alarm mode                                                  | 0x0034    | R/W    |
| SYSTIMER_COMPO_LOAD_REG                     | COMPO synchronization register                                              | 0x0050    | WT     |
| Comparator1 Control and Configuration Registers |                                                                             |           |        |
| SYSTIMER_TARGET1_HI_REG                    | Alarm value to be loaded to COMP1, high 20 bits                             | 0x0024    | R/W    |
| SYSTIMER_TARGET1_LO_REG                     | Alarm value to be loaded to COMP1, low 32 bits                              | 0x0028    | R/W    |
| SYSTIMER_TARGET1_CONF_REG                   | Configure COMP1 alarm mode                                                  | 0x0038    | R/W    |
| SYSTIMER_COMP1_LOAD_REG                     | COMP1 synchronization register                                              | 0x0054    | WT     |
| Comparator2 Control and Configuration Registers |                                                                             |           |        |
| SYSTIMER_TARGET2_HI_REG                    | Alarm value to be loaded to COMP2, high 20 bits                             | 0x002C    | R/W    |
| SYSTIMER_TARGET2_LO_REG                     | Alarm value to be loaded to COMP2, low 32 bits                              | 0x0030    | R/W    |
| SYSTIMER_TARGET2_CONF_REG                   | Configure COMP2 alarm mode                                                  | 0x003C    | R/W    |
| SYSTIMER_COMP2_LOAD_REG                     | COMP2 synchronization register                                              | 0x0058    | WT     |
| Interrupt Registers                        |                                                                             |           |        |
| SYSTIMER_INT_ENA_REG                        | Interrupt enable register of system timer                                    | 0x0064    | R/W    |
| SYSTIMER_INT_RAW_REG                         | Interrupt raw register of system timer                                       | 0x0068    | R/WTC/SS|
| SYSTIMER_INT_CLR_REG                          | Interrupt clear register of system timer                                     | 0x006C    | WT     |
```