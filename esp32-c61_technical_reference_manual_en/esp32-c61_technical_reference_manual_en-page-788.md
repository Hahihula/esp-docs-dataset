

```markdown
| Hash Algorithm | Length of Message Digest (in bits) | Storage¹ |
|----------------|------------------------------------|----------|
| SHA-1          | 160                                | SHA_H_O_REG ~ SHA_H_4_REG |
| SHA-224        | 224                                | SHA_H_O_REG ~ SHA_H_6_REG |
| SHA-256        | 256                                | SHA_H_O_REG ~ SHA_H_7_REG |

¹ The message digest is stored in registers from most significant bits to the least significant bits, with the first word stored in register `SHA_H_O_REG` and the second word stored in register `SHA_H_1_REG... For details, please see subsection 21.4.1.2.
```

## 21.4.4 Interrupt

ESP32-C61's SHA accelerator can generate the following interrupt signal(s) that will be sent to the **Interrupt Matrix**.

*   `SHA_INTR`

There is an internal interrupt source from SHA that can generate the above interrupt signal(s). The interrupt source from SHA is listed with their trigger conditions and the resulted interrupt signal(s) in Table 21.4-2.

Table 21.4-2. SHA's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
|----------------------------|-------------------|------------------|
| `SHA_CALC_DONE_INT`        | Completion of an message digest calculation in DMA-SHA mode | `SHA_INTR` |

**Note:**

*   For definitions of *interrupt*, *interrupt signal*, *interrupt source*, and their correlations, please refer to Chapter 9 **Interrupt Matrix > Section 9.2 Interrupt Terminology in ESP32-O61**.
*   Different from the standard interrupt register group, the interrupt register group of SHA only contains the `INT_ENA` (`SHA_INT_ENA_REG`) and `INT_CLR` (`SHA_INT_CLEAR_REG`) fields, and does not support users to read the `INT_RAW` and `INT_ST` fields.
```