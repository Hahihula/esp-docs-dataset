

```markdown
Y = (\tilde{Y}_{N-1}\tilde{Y}_{N-2} \cdots \tilde{Y}_{t+1}\tilde{Y}_t\tilde{Y}_{t-1} \cdots \tilde{Y}_0)_2

where,

*   N is the length of Y,
*   $\tilde{Y}_i$ is 1,
*   $\tilde{Y}_{N-1}, \tilde{Y}_{N-2}, ..., \tilde{Y}_{t+1}$ are all equal to 0,
*   and $\tilde{Y}_{t-1}, \tilde{Y}_{t-2}, ..., \tilde{Y}_0$ are either 0 or 1 but exactly m bits should be equal to 0 and t-m bits 1, i.e. the Hamming weight of $\tilde{Y}_{t-1}\tilde{Y}_{t-2},\cdots,\tilde{Y}_0$ is $t - m$.

When either of these two options is configured for acceleration:

*   **SEARCH Option (Configuring RSA_SEARCH_ENABLE to 1 for acceleration)**
    *   The accelerator ignores the bit positions of $\tilde{Y}_i$, where i > α. Search position α is set by configuring the RSA_SEARCH_POS_REG register. The maximum value of α is N-1, which leads to the same result when this option is not used for acceleration. The best acceleration performance can be achieved by setting α to t, in which case, all the $\tilde{Y}_{N-1}, \tilde{Y}_{N-2}, ..., \tilde{Y}_{t+1}$ of 0s are ignored during the calculation. Note that if you set α to be less than t, then the result of the modular exponentiation Z = X^Y mod M will be incorrect.
*   **CONSTANT_TIME Option (Configuring RSA_CONST_TIME_REG to 0 for acceleration)**
    *   The accelerator speeds up the calculation by simplifying the calculation concerning the 0 bits of Y. Therefore, the higher the proportion of bits 0 against bits 1, the better the acceleration performance is.

We provide an example to demonstrate the performance of the RSA Accelerator under different combinations of SEARCH and CONSTANT_TIME configuration. Here we perform Z = X^Y mod M with N = 3072 and Y = 65537. Table 20.3-1 below demonstrates the time costs under different combinations of SEARCH and CONSTANT_TIME configuration. Here, we should also mention that, α is set to 16 when the SEARCH option is enabled.

Table 20.3-1. Acceleration Performance

| SEARCH Option | CONSTANT_TIME Option | Time Cost (ms) |
|---------------|----------------------|----------------|
| No acceleration | No acceleration      | 752.81         |
| Accelerated    | No acceleration      | 4.52           |
| No acceleration | Acceleration         | 2.406          |
| Acceleration   | Acceleration         | 2.33           |

It's obvious that:

*   The time cost is the biggest when none of these two options is configured for acceleration.
*   The time cost is the smallest when both of these two options are configured for acceleration.
*   The time cost can be dramatically reduced when either or both option(s) are configured for acceleration.
```