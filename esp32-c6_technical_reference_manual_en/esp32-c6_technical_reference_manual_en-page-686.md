

```markdown
Y = (\tilde{Y}_{N-1}\tilde{Y}_{N-2} \cdots \tilde{Y}_{t+1}\tilde{Y}_t\tilde{Y}_{t-1} \cdots \tilde{Y}_0)_2

where,

*   N is the length of Y,
*   $\tilde{Y}_i$ is 1,
*   $\tilde{Y}_{N-1}, \tilde{Y}_{N-2}, ..., \tilde{Y}_{t+1}$ are all equal to 0,
*   and $\tilde{Y}_{t-1}, \tilde{Y}_{t-2}, ..., \tilde{Y}_0$ are either 0 or 1 but exactly m bits should be equal to 0 and t-m bits 1, i.e. the Hamming weight of $\tilde{Y}_{t-1}\tilde{Y}_{t-2}...,\tilde{Y}_0$ is $t - m$.

When either of these two options is configured for additional acceleration:

*   **SEARCH Option (Configuring RSA_SEARCH_ENABLE to 1 for additional acceleration)**
    *   The accelerator ignores the bit positions of $\tilde{Y}_i$, where i > α. Search position α is set by configuring the RSA_SEARCH_POS_REG register. Set α to a number smaller than N-1, which otherwise leads to the same result as if this option is not used for additional acceleration. The best acceleration performance can be achieved by setting α to t, in which case all the $\tilde{Y}_{N-1}, \tilde{Y}_{N-2}, ..., \tilde{Y}_{t+1}$ of Os are ignored during the calculation. Note that if you set α to be less than t, then the result of the modular exponentiation Z = X^Y mod M will be incorrect.
    *   Note that this option compromises the security because it ignores some bits, which essentially shortens the key length, thus should not be enabled for applications with high security requirement.

*   **CONSTANT_TIME Option (Configuring RSA_CONSTAN_TIME_REG to 0 for additional acceleration)**
    *   The accelerator speeds up the calculation by simplifying the calculation concerning the 0 bits of Y. Therefore, the higher the proportion of bits 0 against bits 1, the better is the acceleration performance.
    *   Note that this option also compromises the security because its time cost correlates with the 0/1 distribution of the key, which can be used in a Side Channel Attack (SCA), thus should not be enabled for applications with high security requirement.

Below is an example to demonstrate the performance of the RSA accelerator under different combinations of SEARCH and CONSTANT_TIME configuration. Here we perform Z = X^Y mod M with N = 3072 and Y = 65537. Table 22.3-1 below demonstrates the time costs under different combinations of SEARCH and CONSTANT_TIME configuration. Here, we should also mention that, α is set to 16 when the SEARCH option is enabled.

Table 22.3-1. Acceleration Performance

| SEARCH Option | CONSTANT_TIME Option | Time Cost (ms) |
|---------------|----------------------|----------------|
| No acceleration | No acceleration | 752.81 |
| Accelerated | No acceleration | 4.52 |
| No acceleration | Acceleration | 2.41 |
| Acceleration | Acceleration | 2.33 |
```