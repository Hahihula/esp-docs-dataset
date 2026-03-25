

```markdown
| Hash Algorithm | Length of Message Digest (in bits) | Storage¹ |
|----------------|------------------------------------|----------|
| SHA-1          | 160                                | SHA_H_O_REG ~ SHA_H_4_REG |
| SHA-224        | 224                                | SHA_H_O_REG ~ SHA_H_6_REG |
| SHA-256        | 256                                | SHA_H_O_REG ~ SHA_H_7_REG |

¹ The message digest is stored in registers from most significant bits to the least significant bits, with the first word stored in register `SHA_H_O_REG` and the second word stored in register `SHA_H_1_REG... For details, please see subsection 23.4.1.2.
```

## 23.4.4 Interrupt

When working in the DMA-SHA mode, SHA supports interrupt on the completion of message digest calculation.

- To enable this function: write 1 to register `SHA_INT_ENA_REG`.
- Note that the interrupt should be cleared by software after use via setting the `SHA_INT_CLEAR_REG` register to 1.

When working in the Typical SHA mode, SHA completes the calculation quickly, so an interrupt is not necessary. Therefore, SHA does not support interrupt in the Typical SHA mode.
```