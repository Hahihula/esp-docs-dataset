**Title:**
Table 9.3-1. CPU Peripheral Interrupt Configuration/Status Registers and Peripheral Interrupt Sources

**Columns in Table:**
1. No.
2. Source
3. Configuration Register
4. Bit Name

**Content of the Table (Sample Rows):**

| No. | Source                | Configuration Register                                      | Bit  Name |
|-----|-----------------------|-------------------------------------------------------------|-----------|
| O   | MAC_INTR              | INTERRUPT\Corex_MACINTR_MAP_REG                           | 0         |
| 1   | MAC_NMI               | INTERRUPT\Corex_MAC_NMI_MAP_REG                           | 1         |
| 2   | PWR_INTR              | INTERRUPT\Corex_PWR_INTR_MAP_REG                          | 2         |
| 3   | BB_INT                | INTERRUPT\Corex_BB_INT_MAP_REG                            | 3         |
| 4   | BT_MAC_INT            | INTERRUPT\Corex_BT_MACINT_MAP_REG                         | 4         |
| 5   | BT_BB_INT             | INTERRUPT\Corex_BT_BB_INTP_MAP_REG                        | 5         |
| 6   | BT_BB_NMI             | INTERRUPT\Corex_BT_BB_NMI_MAP_REG                         | 6         |
| 7   | RWBT IRQ              | INTERRUPT\Corex_RWBT_IRQ_MAP_REG                          | 7         |
| ... | ...                   | ...                                                         | ...       |

**Additional Notes:**
- Some entries are marked as "reserved".
- The table continues with more rows, each detailing a different interrupt source and its corresponding configuration register.
- There is an indication of the bit name for some registers (e.g., INTERRUPT\Corex_INTR_STATUS_0_REG).