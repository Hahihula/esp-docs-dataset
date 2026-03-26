

```markdown
- Step 6: Calculate $C = [C]_{12672} = \text{AES-CBC-ENC}([P]_{12672}, [RSA\_DS\_KEY]_{256}, [IV]_{128})$, where C is the ciphertext with a length of 1200 bytes. $C$ can also be calculated as $C = [C]_{12672} = (\overline{[Y]}_{4096}||\widehat{[M]}_{4096}||\widehat{[\overline{r}]}_{4096}||[\widehat{\text{Box}}]_{384})$, where $\overline{[Y]}_{4096}$, $[\widehat{M}]_{4096}$, $[\widehat{\overline{r}}]_{4096}$, $[\widehat{\text{Box}}]_{384}$ are the four sub-parameters of C, and correspond to the ciphertext of $[Y']_{4096}$, $[M']_{4096}$, $[\overline{r}']_{4096}$, $[\text{Box}']_{384}$ respectively.

### 30.3.4 RSA_DS Operation at the Hardware Level

The hardware operation is triggered each time a digital signature needs to be calculated. The inputs are the pre-generated private key ciphertext C, a unique message X, and IV.

The RSA_DS operation at the hardware level can be divided into the following three stages:

1. **Decryption: Step 7 and 8 in Figure 30.3-1**

   The decryption process is the inverse of Step 6 in Figure 30.3-1. The RSA_DS peripheral will call the AES accelerator to decrypt C in CBC block mode and get the resulting plaintext. The decryption process can be represented by $P = \text{AES-CBC-DEC}(C, RSA\_DS\_KEY, IV)$, where IV (i.e., $[IV]_{128}$) is defined by the user. $[RSA\_DS\_KEY]_{256}$ is

   - when calculated by the RSA_DS peripheral via the HMAC peripheral: provided by the HMAC module, derived from `HMAC_KEY` stored in eFuse, which is not readable by users.
   - when from Key Manager module: `RSA_DS_KEY` deployed by Key Manager, which is not readable by users.

   With P, the RSA_DS peripheral can derive $[Y]_{4096}$, $[M]_{4096}$, $[\overline{r}]_{4096}$, $[M']_{32}$, $[L]_{32}$, MD authentication code, and the padding value $[\beta]_{64}$. This process is the inverse of Step 5.

2. **Check: Step 9 and 10 in Figure 30.3-1**

   The RSA_DS peripheral will perform two checks: MD check and padding check. The padding check is not shown in Figure 30.3-1, as it happens at the same time as the MD check.

   - **MD check**: The RSA_DS peripheral calls SHA-256 to calculate the hash value $[CALC\_MD]_{256}$ ($([CALC\_MD]_{256})$ is calculated the same way and with same parameters as $[MD]_{256}$, see step 4). Then, $[CALC\_MD]_{256}$ is compared against the MD authentication code $[MD]_{256}$ from step 4. Only when the two match does the MD check pass.
   - **Padding check**: The RSA_DS peripheral checks if $[\beta]_{64}$ complies with the aforementioned PKCS#7 format. Only when $[\beta]_{64}$ complies with the format does the padding check pass.

   The RSA_DS peripheral will only perform subsequent operations if MD check passes. If the padding check fails, a warning is generated, but it does not affect the subsequent operations.

3. **Calculation: Step 11 and 12 in Figure 30.3-1**

   The RSA_DS peripheral treats X (input by the user) and Y, M, $\overline{r}$ (decrypted in step 8) as big numbers. With $M'$, all operands to perform $X^Y \mod M$ are in place. The operand length is defined by L only. The RSA_DS peripheral will calculate the signed result Z by calling RSA to perform $Z = X^Y \mod M$.

### 30.3.5 RSA_DS Operation at the Software Level

The software steps below should be followed each time a digital signature needs to be calculated. The inputs are the pre-generated private key ciphertext C, a unique message X, and IV. These software steps trigger
```