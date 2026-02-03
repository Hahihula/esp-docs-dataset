**Chapter Title:**
Chapter 22 Digital Signature (DS)

**Section Titles and Content:**

### **22.3.4 DS Operation at the Hardware Level**

The hardware operation is triggered each time a digital signature needs to be calculated. The inputs are the pre-generated private key ciphertext \( C \), a unique message \( X \), and \( IV \).

The DS operation at the hardware level can be divided into the following three stages:

1. **Decryption: Step 7 and 8 in Figure 22.3-1**

   - The decryption process is the inverse of Step 6 in figure [22.3-1](#). The DS peripheral will call AES accelerator to decrypt \( C \) in CBC block mode and get the resulted plaintext.
     - The decryption process can be represented by:
       \[
       P = AES-CBC-DEC (C, DS_KEY, IV)
       \]
       where \( IV \) is defined by users. 
       \[
       [DS\_KEY]_{256}
       \]
       provided by HMAC module, derived from \( HMAC\_KEY \) stored in eFuse.
     - The resulting values are not readable by users.

   With P, the DS peripheral can derive:
   \[
   Y = 4096
   \]
   \[
   M = 4096
   \]
   \[
   \bar{Y} = 4096
   \]
   \[
   [M']_{32}
   \]
   MD authentication code, and the padding value \( [\beta]_{64} \).
   - This process is the inverse of Step 5.

2. **Check: Step 9 and 10 in Figure 22.3-1**

   The DS peripheral will perform two checks:
   - MD check
     - The DS peripheral calls SHA-256 to calculate the MD authentication code \( [CALC\_MD]_{256} \) from pre-calculated values.
       \[
       Y = 4096
       \]
       \[
       M = 4096
       \]
       \[
       \bar{Y} = 4096
       \]
       \[
       [M']_{32}
       \]
       \[
       IV = 128
       \]
     - The calculated \( CALC\_MD \) is compared against the pre-calculated MD authentication code.
   - Padding check:
     - The DS peripheral checks if \( [\beta]_{64} \) complies with PKCS#7 format. Only when it passes, padding check also succeeds.

3. **Calculation: Step 11 and 12 in Figure 22.3-1**

   The DS peripheral treats:
   - \( X^Y \)
   - \( M \)
   - \( T \) (compiled as big numbers).
   With \( M' \), all operands to perform the calculation.
   - The operand length is defined by L.

### **22.3.5 DS Operation at the Software Level**

The following software steps should be followed each time a Digital Signature needs to be calculated:
- Inputs are pre-generated private key ciphertext, unique message \( X \), and \( IV \).
- These operations trigger hardware described in Section 22.3.4.

Assume that software has called HMAC peripheral on the hardware with calculated \( DS\_KEY \) based on \( HMAC\_KEY \).

1. **Prerequisites:**
   - Prepare operands, C, X, IV according to [Section 22.3-3](#).
   
2. **Activate the DS peripheral:** Write `1` to `DS_SET_START_REG`.

**Footer Information:**

Espressif Systems  
901 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback