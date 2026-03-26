

```markdown
## 29.4.1.3 Setting the Initial Hash Value

Before hash task begins for each of the secure hash algorithms, the initial Hash value H⁽⁰⁾ must be set based on different algorithms, among which the SHA-1, SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224, and SHA-512/256 algorithms use the initial Hash values (constant C) stored in the hardware.

However, SHA-512/t requires a distinct initial hash value for each operation for a given value of t. Simply put, SHA-512/t is the generic name for a t-bit hash function based on SHA-512 whose output is truncated to t bits. t is any positive integer without a leading zero such that t<512, and t is not 384. The initial hash value for SHA-512/t for a given value of t can be calculated by performing SHA-512 from hexadecimal representation of the string “SHA-512/t”. It’s not hard to observe that when determining the initial hash values for SHA-512/t algorithms with different t, the only difference lies in the value of t.

Therefore, we have specially developed the following simplified method to calculate the initial hash value for SHA-512/t:

1. Generate t_string and t_length: t_string is a 32-bit data that stores the input message of t. t_length is a 7-bit data that stores the length of the input message. The t_string and t_length are generated in methods described below, depending on the value of t:

    * If 1 <= t <= 9, then t_length = 7’h48 and t_string is padded in the following format:
        ```
        | 8'h30 + 8'ht₀ | 1'b1 | 23'b0 |
        ```
        where t₀ = t.

        For example, if t = 8, then t₀ = 8 and t_string = 32’h38800000.

    * If 10 <= t <= 99, then t_length = 7’h50 and t_string is padded in the following format:
        ```
        | 8'h30 + 8'ht₁ | 8'h30 + 8'ht₀ | 1'b1 | 15'b0 |
        ```
        where, t₀ = t%10 and t₁ = t/10.

        For example, if t = 56, then t₀ = 6, t₁ = 5, and t_string = 32’h35368000.

    * If 100 <= t < 512, then t_length = 7’h58 and t_string is padded in the following format:
        ```
        | 8'h30 + 8'ht₂ | 8'h30 + 8'ht₁ | 8'h30 + 8'ht₀ | 1'b1 | 7'b0 |
        ```
        where, t₀ = t%10, t₁ = (t/10)%10, and t₂ = t/100.

        For example, if t = 231, then t₀ = 1, t₁ = 3, t₂ = 2, and t_string = 32’h32333180.

2. Initialize relevant registers: Initialize SHA_T_STRING_REG and SHA_T_LENGTH_REG with the generated t_string and t_length in the previous step.

3. Obtain initial hash value: Set the SHA_MODE_REG register to 7. Set the SHA_START_REG register to 1 to start the SHA accelerator. Then poll register SHA_BUSY_REG until the content of this register becomes 0, indicating the calculation of initial hash value is completed.

Please note that the initial value for SHA-512/t can be also calculated according to the Section “5.3.6 SHA-512/t” in FIPS PUB 180-4 Spec., which is performing SHA-512 operation (with its initial hash value set to the result of 8-bitwise XOR operation of C and Oxa5) from the hexadecimal representation of the string “SHA-512/t”.
```