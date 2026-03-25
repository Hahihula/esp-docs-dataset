
```markdown
| Name                                       | Description                                                                 | Address | Access   |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|----------|
| Interrupt Registers                        |                                                                             |         |          |
| ECC_MULT_INT_RAW_REG                       | ECC raw interrupt status register                                           | 0x000C  | R/SS/WTC |
| ECC_MULT_INT_ST_REG                        | ECC masked interrupt status register                                       | 0x0010  | RO       |
| ECC_MULT_INT_ENA_REG                       | ECC interrupt enable register                                               | 0x0014  | R/W      |
| ECC_MULT_INT_CLR_REG                       | ECC interrupt clear register                                                 | 0x0018  | WT       |
| Configuration Register                     |                                                                             |         |          |
| ECC_MULT_CONF_REG                          | ECC configuration register                                                  | 0x001C  | varies   |
| Version Register                           |                                                                             |         |          |
| ECC_MULT_DATE_REG                          | Version control register                                                    | 0x00FC  | R/W      |
```