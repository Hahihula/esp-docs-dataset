
```markdown
## 22.3.4 DS Operation at the Hardware Level

The hardware operation is triggered each time a digital signature needs to be calculated. The inputs are the pre-generated private key ciphertext C, a unique message X, and IV.

The DS operation at the hardware level can be divided into the following three stages:

1.  **Decryption: Step 7 and 8 in Figure 22.3-1**

    The decryption process is the inverse of Step 6 in figure 22.3-1. The DS module will call AES accelerator to decrypt C in CBC block mode and get the resulted plaintext. The decryption process can be represented by P = AES-CBC-DEC (C, DS_KEY, IV), where IV (i.e., [IV]₁₂₈) is defined by you. [DS_KEY]₂₅₆ is provided by HMAC module, derived from HMAC_KEY stored in eFuse. [DS_KEY]₂₅₆, as well as [HMAC_KEY]₂₅₆ are not readable by users. For more information, please refer to Chapter 19 HMAC Accelerator (HMAC).

    With P, the DS module can derive [Y]₃₀₇₂, [M]₃₀₇₂, [r̄]₃₀₇₂, [M′]₃₂, [L]₃₂, MD authentication code, and the padding value [β]₆₄. This process is the inverse of Step 5.

2.  **Check: Step 9 and 10 in Figure 22.3-1**

    The DS module will perform two checks: MD check and padding check. Padding check is not shown in Figure 22.3-1, as it happens at the same time with MD check.

    *   MD check: The DS module calls SHA-256 to calculate the hash value [CALC_MD]₂₅₆ (i.e., step 4). Then, [CALC_MD]₂₅₆ is compared against the MD authentication code [MD]₂₅₆ from step 4. Only when the two match does the MD check pass.

    *   Padding check: The DS module checks if [β]₆₄ complies with the aforementioned PKCS#7 format. Only when [β]₆₄ complies with the format does the padding check pass.

    The DS module will only perform subsequent operations if MD check passes. If padding check fails, a warning message is generated, but it does not affect the subsequent operations.

3.  **Calculation: Step 11 and 12 in Figure 22.3-1**

    The DS module treats X (input by you) and Y, M, r̄ (compiled) as big numbers. With M′, all operands to perform X^Y mod M are in place. The operand length is defined by L only. The DS module will get the signed result Z by calling RSA to perform Z = X^Y mod M.

## 22.3.5 DS Operation at the Software Level

The software steps below should be followed each time a digital signature needs to be calculated. The inputs are the pre-generated private key ciphertext C, a unique message X, and IV. These software steps trigger the hardware steps described in Section 22.3.4.

We assume that the software has called the HMAC peripheral and HMAC on the hardware has calculated DS_KEY based on HMAC_KEY.

1.  **Prerequisites:** Prepare operands C, X, IV according to Section 22.3.3.
2.  **Activate the DS peripheral:** Write 1 to DS_SET_START_REG.
3.  **Check if DS_KEY is ready:** Poll DS_QUERY_BUSY_REG until the software reads 0.
```