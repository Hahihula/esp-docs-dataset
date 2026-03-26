

```markdown
Users can choose to use one or two of these options to further accelerate the computation. Note that, even when none of these two options is configured, using the hardware RSA accelerator is still much faster than implementing the RSA algorithm in software.

To be more specific, when neither of these two options are configured for additional acceleration, the time required to calculate Z = X^Y mod M is solely determined by the lengths of operands. When either or both of these two options are configured for additional acceleration, the time required is also correlated with the 0 and 1 bit distribution in Y.

To better illustrate how these two options work, first assume Y is represented in binaries as

    Y = (Ŷ_{N−1} Ŷ_{N−2} ⋯ Ŷ_{t+1} Ŷ_t Ŷ_{t−1} ⋯ Ŷ_0)_2

where,

* N is the length of Y,
* Ŷ_i is 1,
* Ŷ_{N−1}, Ŷ_{N−2}, ..., Ŷ_{t+1} are all equal to 0,
* and Ŷ_{t−1}, Ŷ_{t−2}, ..., Ŷ_0 are either 0 or 1 but exactly m bits should be equal to 0 and t−m bits 1, i.e., the Hamming weight of Ŷ_{t−1} Ŷ_{t−2}, ..., Ŷ_0 is t − m.

When either of these two options is configured for additional acceleration:

* SEARCH Option (Configuring RSA_SEARCH_ENABLE to 1 for additional acceleration)

    - The accelerator ignores the bit positions of Ŷ_i, where i > α. Search position α is set by configuring the RSA_SEARCH_POS_REG register. Set α to a number smaller than N−1, which otherwise leads to the same result as if this option is not used for additional acceleration. The best acceleration performance can be achieved by setting α to t, in which case all the Ŷ_{N−1}, Ŷ_{N−2}, ..., Ŷ_{t+1} of 0 s are ignored during the calculation. Note that if you set α to be less than t, then the result of the modular exponentiation Z = X^Y mod M will be incorrect.
    - Note that this option compromises the security because it ignores some bits, which essentially shortens the key length, thus should not be enabled for applications with high security requirement.

* CONSTANT_TIME Option (Configuring RSA_CONSTANT_TIME_REG to 0 for additional acceleration)

    - The accelerator speeds up the calculation by simplifying the calculation concerning the 0 bits of Y. Therefore, the higher the proportion of bits 0 against bits 1, the better is the acceleration performance.
    - Note that this option also compromises the security because its time cost correlates with the 0/1 distribution of the key, which can be used in a Side Channel Attack (SCA), thus should not be enabled for applications with high security requirement.

Below is an example to demonstrate the performance of the RSA accelerator under different combinations of SEARCH and CONSTANT_TIME configuration. In this example:

* We perform Z = X^Y mod M
* N = 3072
```