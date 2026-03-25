

```markdown
| SEARCH Option | CONSTANT_TIME Option | Time Cost (clock cycle) |
|---------------|----------------------|-------------------------|
| No acceleration | No acceleration | 174.7 × 10^6 |
| Acceleration | No acceleration | 1.023 × 10^6 |
| No acceleration | Acceleration | 0.546 × 10^6 |
| Acceleration | Acceleration | 0.540 × 10^6 |

As shown in Table 25.3-1:
* The time cost is the biggest when none of these two options is configured for additional acceleration.
* The time cost is the smallest when both of these two options are configured for additional acceleration.
* The time cost can be dramatically reduced when either or both option(s) are configured for additional acceleration.

## 25.4 Interrupts

ESP32-C5's RSA accelerator can generate the following interrupt signal that will be sent to the [Interrupt Matrix](#).
* RSA_INTR

There is one internal interrupt source from the RSA accelerator that can generate the above interrupt signal.
The interrupt source from the RSA accelerator is listed with its trigger condition and the resulting interrupt signal in Table 25.4-1.

Table 25.4-1. RSA's Internal Interrupt Source
| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
|----------------------------|-------------------|------------------|
| RSA_CALC_DONE_INT          | Completion of an RSA calculation | RSA_INTR |

**Note:**
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 11 [Interrupt Matrix > Section 11.2 Terminology](#).
```