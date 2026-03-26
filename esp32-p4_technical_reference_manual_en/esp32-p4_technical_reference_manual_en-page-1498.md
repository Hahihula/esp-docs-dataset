

```markdown
| Hash Algorithm | Length of Message Digest (in bits) | Storage¹ |
|----------------|------------------------------------|----------|
| SHA-1          | 160                                | SHA_H_O_REG ~ SHA_H_4_REG |
| SHA-224        | 224                                | SHA_H_O_REG ~ SHA_H_6_REG |
| SHA-256        | 256                                | SHA_H_O_REG ~ SHA_H_7_REG |
| SHA-384        | 384                                | SHA_H_O_REG ~ SHA_H_11_REG |
| SHA-512        | 512                                | SHA_H_O_REG ~ SHA_H_15_REG |
| SHA-512/224    | 224                                | SHA_H_O_REG ~ SHA_H_6_REG |
| SHA-512/256    | 256                                | SHA_H_O_REG ~ SHA_H_7_REG |
| SHA-512/t²     | t                                  | SHA_H_O_REG ~ SHA_H_X_REG |

---

¹ The message digest is stored in registers from most significant bits to the least significant bits, with the first word stored in register `SHA_H_O_REG` and the second word stored in register `SHA_H_1_REG`. For details, please see subsection 29.4.1.2.

² The registers used for SHA-512/t algorithm depend on the value of t. x+1 indicates the number of 32-bit registers used to store t bits of message digest, so that `x = roundup(t/32) - 1`. For example:

• When t = 8, then x = 0, indicating that the 8-bit long message digest is stored in the most significant 8 bits of register `SHA_H_O_REG`;

• When t = 32, then x = 0, indicating that the 32-bit long message digest is stored in register `SHA_H_O_REG`;

• When t = 132, then x = 4, indicating that the 132-bit long message digest is stored in registers `SHA_H_O_REG`, `SHA_H_1_REG`, `SHA_H_2_REG`, `SHA_H_3_REG`, and `SHA_H_4_REG`.

---

## 29.5 Interrupt

ESP32-P4's SHA accelerator can generate the following interrupt signal(s) that will be sent to the **Interrupt Matrix**.

*   SHA_INTR

There are several internal interrupt sources from SHA that can generate the above interrupt signal(s). The interrupt sources from SHA are listed with their trigger conditions and the resulted interrupt signal(s) in Table 29.5-1.

Table 29.5-1. SHA's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
|----------------------------|-------------------|------------------|
| SHA_CALC_DONE_INT          | Completion of an message digest calculation in DMA-SHA mode | SHA_INTR |

---

**Note:**

*   For definitions of `interrupt`, `interrupt signal`, `interrupt source`, and their correlations, please refer to Chapter 12
```