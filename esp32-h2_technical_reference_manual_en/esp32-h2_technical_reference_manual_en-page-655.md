

```markdown
Chapter 24 Digital Signature Algorithm (DSA) GoBack

of C, and correspond to the ciphertext of [Y]3072, [M]3072, [r̄]3072, [Box]384 respectively.

24.3.4 DSA Operation at the Hardware Level

The hardware operation is triggered each time a digital signature needs to be calculated. The inputs are the pre-generated private key ciphertext C, a unique message X, and IV.
The DSA operation at the hardware level can be divided into the following three stages:

1. Decryption: Step 7 and 8 in Figure 24.3-1

The decryption process is the inverse of Step 6 in Figure 24.3-1. The DSA module will call the AES accelerator to decrypt C in CBC block mode and get the resulting plaintext. The decryption process can be represented by P = AES-CBC-DEC (C, DSA_KEY, IV), where IV (i.e., [IV]128) is defined by the user. [DSA_KEY]256 is provided by the HMAC module, derived from HMAC_KEY stored in eFuse. [DSA_KEY]256, as well as [HMAC_KEY]256 are not readable by users. or more information, please refer to Chapter 21 HMAC Accelerator (HMAC).

With P, the DSA module can derive [Y]3072, [M]3072, [r̄]3072, [M′]32, [L]32, MD authentication code, and the padding value [β]64. This process is the inverse of Step 5.

2. Check: Step 9 and 10 in Figure 24.3-1

The DSA module will perform two checks: MD check and padding check. The padding check is not shown in Figure 24.3-1, as it happens at the same time as the MD check.

• MD check: The DSA module calls SHA-256 to calculate the hash value [CALC_MD]256 ([CALC_MD]256 is calculated the same way and with same parameters as [MD]256, see step 4). Then, [CALC_MD]256 is compared against the MD authentication code [MD]256 from step 4. Only when the two match does the MD check pass.

• Padding check: The DSA module checks if [β]64 complies with the aforementioned PKCS#7 format. Only when [β]64 complies with the format does the padding check pass.

The DSA module will only perform subsequent operations if MD check passes. If the padding check fails, a warning is generated, but it does not affect the subsequent operations.

3. Calculation: Step 11 and 12 in Figure 24.3-1

The DSA module treats X (input by the user) and Y, M, π (decrypted in step 8) as big numbers. With M′, all operands to perform XY mod M are in place. The operand length is defined by L only. The DSA module will calculate the signed result Z by calling RSA to perform Z = XY mod M.

24.3.5 DSA Operation at the Software Level

The software steps below should be followed each time a digital signature needs to be calculated. The inputs are the pre-generated private key ciphertext C, a unique message X, and IV. These software steps trigger the hardware steps described in Section 24.3.4.

We assume that the software has called the HMAC peripheral and the HMAC peripheral has calculated DSA_KEY based on HMAC_KEY.

1. Prerequisites: Prepare operands C, X, IV according to Section 24.3.3.
2. Activate the DSA peripheral: Write 1 to DS_SET_START_REG.
```