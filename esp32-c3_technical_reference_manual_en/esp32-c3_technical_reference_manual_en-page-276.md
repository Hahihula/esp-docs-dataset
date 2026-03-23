

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| SYSTIMER_UNIT1_LOAD_REG                   | UNIT1 synchronization register                                              | 0x0060    | WT     |
| Comparator⁰ Control and Configuration Registers |                                                                             |           |        |
| SYSTIMER_TARGETO_HI_REG                   | Alarm value to be loaded to COMPO, high 20 bits                            | 0x001C    | R/W    |
| SYSTIMER_TARGETO_LO_REG                   | Alarm value to be loaded to COMPO, low 32 bits                             | 0x0020    | R/W    |
| SYSTIMER_TARGETO_CONF_REG                 | Configure COMPO alarm mode                                                  | 0x0034    | R/W    |
| SYSTIMER_COMPO_LOAD_REG                   | COMPO synchronization register                                              | 0x0050    | WT     |
| Comparator¹ Control and Configuration Registers |                                                                             |           |        |
| SYSTIMER_TARGET1_HI_REG                   | Alarm value to be loaded to COMP1, high 20 bits                            | 0x0024    | R/W    |
| SYSTIMER_TARGET1_LO_REG                   | Alarm value to be loaded to COMP1, low 32 bits                             | 0x0028    | R/W    |
| SYSTIMER_TARGET1_CONF_REG                 | Configure COMP1 alarm mode                                                  | 0x0038    | R/W    |
| SYSTIMER_COMP1_LOAD_REG                   | COMP1 synchronization register                                              | 0x0054    | WT     |
| Comparator² Control and Configuration Registers |                                                                             |           |        |
| SYSTIMER_TARGET2_HI_REG                   | Alarm value to be loaded to COMP2, high 20 bits                            | 0x002C    | R/W    |
| SYSTIMER_TARGET2_LO_REG                   | Alarm value to be loaded to COMP2, low 32 bits                             | 0x0030    | R/W    |
| SYSTIMER_TARGET2_CONF_REG                 | Configure COMP2 alarm mode                                                  | 0x003C    | R/W    |
| SYSTIMER_COMP2_LOAD_REG                   | COMP2 synchronization register                                              | 0x0058    | WT     |
| Interrupt Registers                                                                             |           |        |
| SYSTIMER_INT_ENA_REG                      | Interrupt enable register of system timer                                   | 0x0064    | R/W    |
| SYSTIMER_INT_RAW_REG                      | Interrupt raw register of system timer                                      | 0x0068    | R/WTC/SS|
| SYSTIMER_INT_CLR_REG                      | Interrupt clear register of system timer                                    | 0x006C    | WT     |
| SYSTIMER_INT_ST_REG                       | Interrupt status register of system timer                                   | 0x0070    | RO     |
| Version Register                                                                                 |           |        |
| SYSTIMER_DATE_REG                         | Version control register                                                    | 0x00FC    | R/W    |
```