**Title: Chapter 22 Digital Signature (DS)**

---

### Software level vs Hardware level Flowchart:
- **Software level**
  1. Make Y, M, DS_KEY and IV ready.
  2. Calculate r and M'.
  3. Extend γ, M, r.
  4. Invoke SHA256 to calculate MD.
  5. Build [P]_{12672}.
  6. CBC encryption.

- **Hardware level**
  - (Steps are not explicitly listed in the image)

---

**Figure Caption: Figure 22.3-1. Software Preparations and Hardware Working Process**

---

### Note:
1. The software preparation (left side of the figure) is a one-time operation before any signature is calculated, while the hardware calculation (right side of the figure - 1) repeats for every signature calculation.

---

**Body Text:**
Users need to follow the steps shown in the left part of Figure [22.3-1](#) to calculate C. Detailed instructions are as follows:

### Step-by-step Instructions:
- **Step 1:** Prepare operands Y' and M whose lengths should meet the requirements in Section [22.3.2](#). Define L_{32} = N_{32} - 1 (i.e., for RSA 4096, L_{32} == [0x80-1]_{32}). Prepare [HMAC_KEY]_{256} and calculate [DS_KEY]_{256} based on DS_KEY = HMAC-SHA256 ([HMAC_KEY]_{256}, 1^{256}). Generate a random IV_{128} which should meet the requirements of the AES-CBC block encryption algorithm. For more information on AES, please refer to Chapter [19 AES Accelerator](#).

- **Step 2:** Calculate r and M' based on M.

- **Step 3:** Extend Y, M, and F, in order to get [Y]_{4096}, [M]_{4096} and [F]_{4096}. This step is only required for Y, M and F whose length are less than 4096 bits since their largest length is 4096 bits.

- **Step 4:** Calculate MD authentication code using the SHA-256: [MD]_{256} = SHA256 ([Y]_{4096} || [M]_{4096} || ... || [F]_{4096}) || [IV]_{128}.

- **Step 5:** Build [P]_{12672} = ([Y]_{4096} || [M]_{4096} || ... || [F]_{4096}) || [MD]_{256} || [IV]_{128}, where [β]_{64} is a PKCS#7 padding value, i.e., 64-bit string (value = 0x80) composed of 8 bytes. The purpose of [β]_{64} is to make the bit length of P a multiple of 128.

- **Step 6:** Calculate C = [C]_{12672} = AES-CBC-ENC ([P]_{12672}, [DS_KEY]_{256}, [IV]_{128}), where C is the ciphertext with length of 12672 bits.

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

900 ESP32-S3 TRM (Version 1.7)