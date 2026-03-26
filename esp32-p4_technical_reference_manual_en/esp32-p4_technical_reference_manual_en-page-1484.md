

```markdown
• Y = 65537  
• X and M are taken at random  
• When the SEARCH option is enabled, α, i.e., the position register RSA_SEARCH_POS_REG, is set to 16.
```

Table 28.3-1 below demonstrates the time cost in clock cycles under different combinations of SEARCH and CONSTANT_TIME configuration when performing Z = X^Y mod M as described above.

Table 28.3-1. Acceleration Performance

| SEARCH Option | CONSTANT_TIME Option | Time Cost (clock cycle) |
|---------------|----------------------|-------------------------|
| No acceleration | No acceleration | 174.7 × 10⁶ |
| Accelerated | No acceleration | 1.023 × 10⁶ |
| No acceleration | Acceleration | 0.546 × 10⁶ |
| Acceleration | Acceleration | 0.540 × 10⁶ |

As shown in Table 28.3-1:

* The time cost is biggest when none of these two options is configured for additional acceleration.
* The time cost is smallest when both of these two options are configured for additional acceleration.
* The time cost can be dramatically reduced when either or both option(s) are configured for additional acceleration.

## 28.4 Interrupts

ESP32-P4’s RSA accelerator can generate the following interrupt signal that will be sent to the **Interrupt Matrix**.

• RSA_INTR

There is one internal interrupt source from the RSA accelerator that can generate the above interrupt signal. The interrupt source from the RSA accelerator is listed with its trigger condition and the resulting interrupt signal in Table 28.4-1.

Table 28.4-1. RSA’s Internal Interrupt Source

| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
|----------------------------|-------------------|------------------|
| RSA_CALC_DONE_INT          | Completion of an RSA calculation | RSA_INTR |

**Note:**

For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 **Interrupt Matrix > Section 12.2 Interrupt Terminology** in ESP32-P4.
```