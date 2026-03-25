
```markdown
Figure 24.3-1. Software Preparations and Hardware Working Process

Note:
1. The software preparation (left side in Figure 24.3-1) is a one-time operation before any signature is calculated, while the hardware calculation (right side in Figure 24.3-1) repeats for every signature calculation.
2. Software preparation requires configuring the clock reset. For more information, please refer to Chapter 7 Reset and Clock.

Users need to follow the steps shown in the left part of Figure 24.3-1 to calculate C. Detailed instructions are as follows:

• Step 1: Prepare operands Y and M whose lengths should meet the requirements in Section 24.3.2.
Define [L]₃₂ = N/32 − 1 (i.e., for RSA 3072, [L]₃₂ == [0x60-1]₃₂). Prepare [HMAC_KEY]₂₅₆ and calculate [DSA_KEY]₂₅₆ based on DSA_KEY = HMAC-SHA256 ([HMAC_KEY]₂₅₆, 1²⁵⁶). Generate a random [IV]₁₂₈ which should meet the requirements of the AES-CBC block encryption algorithm. For more information on AES, please refer to Chapter 19 AES Accelerator (AES).

• Step 2: Calculate r and M' based on M.

• Step 3: Extend Y, M, and r̄ in order to get [Y]₃₀₇₂, [M]₃₀₇₂, and [r̄]₃₀₇₂, respectively. This step is only required for Y, M, and r̄ whose length are less than 3072 bits, since their largest length are 3072 bits.

• Step 4: Calculate MD authentication code using the SHA-256:
[MD]₂₅₆ = SHA256 ([Y]₃₀₇₂||[M]₃₀₇₂||[r̄]₃₀₇₂||[M']₃₂||[L]₃₂||[IV]₁₂₈)

• Step 5: Build [P]₉₆₀₀ = ( [Y]₃₀₇₂||[M]₃₀₇₂||[r̄]₃₀₇₂||[Box]₃₈₄), where Box₃₈₄ = (
[MD]₂₅₆||[M']₃₂||[L]₃₂||[β]₆₄) and [β]₆₄ is a PKCS#7 padding value, i.e., a [0x0808080808080808]₆₄ string composed of 8 bytes (0x80). The purpose of [β]₆₄ is to make the bit length of P a multiple of 128.

• Step 6: Calculate C = [C]₉₆₀₀ = AES-CBC-ENC ([P]₉₆₀₀, [DSA_KEY]₂₅₆, [IV]₁₂₈), where C is the ciphertext with a length of 1200 bytes. C can also be calculated as C = [C]₉₆₀₀ =
([Ŷ]₃₀₇₂||[M̂]₃₀₇₂||[r̄̂]₃₀₇₂||[Box̂]₃₈₄), where [Ŷ]₃₀₇₂, [M̂]₃₀₇₂, [r̄̂]₃₀₇₂, [Box̂]₃₈₄ are the four sub-parameters
```