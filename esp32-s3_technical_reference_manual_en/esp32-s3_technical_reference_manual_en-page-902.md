Title: Chapter 22 Digital Signature (DS)

**3. Check if DS_KEY is read**
- Poll DS_QUERY_BUSY_REG until the software reads O.
- If the software does not read O in DS_QUERY_BUSY_REG after approximately 1 ms, it indicates a problem with HMAC initialization. In such cases, you can check DS_QUERY_KEY WRONG REG to get more information:
  - If the software reads O in DS_QUERY_KEY WRONG REG, this means that the HMAC peripheral has not been activated.
  - If the software reads any value from 1 to 15 in DS_QUERY_KEY WRONG REG, it indicates that HMAC was activated but the DS peripheral did not successfully receive the DS_KEY value from the HMAC peripheral. This may indicate a problem with the HMAC operation due to concurrency issues.

**4. Configure register**
- Write IV block to register DS_IV_M_REG (m: 0-3). For more information on the IV block, refer to Chapter 19 AES Accelerator.
- Write X to memory block DS_X_MEM; write \(X_i\) where \(i = \{0, 1,..., n - 1\}\), and for each word in this range:
  - Memory blocks have a capacity of 128 words. Each can store one base-b digit (where b is the least significant digit).
  - The memory block uses little-endian format.
- Words from DS_X_MEM are ignored after the configured length \(X\) bits, as described in Section 22.3.2.

**5. Write C to memory block DS_C_MEM**
- Write \(C_i\) (where \(i = \{0, 1,..., 395\}\)) for each word.
- Memory capacity is specified by the base-b digit format; it can store one b-digit per word in this range.

**6. Start DS operation:**
- Write to register DS_SET_ME_REG.

**7. Wait for the operation to be completed**

**8. Query check result:**
- Read from register DS_QUERY_CHECK_REG and determine subsequent operations based on return value:
  - If \(0\), both padding checks pass.
  - If \(1\), padding passes but MD check fails; continue with signed result Z.
  - If \(2\), padding fail, proceed to step for signed results.

**9. Read the signed result:**
- Read from memory block DS_Z_MEM (where n = \(\frac{N}{32}\)) and store in little-endian byte order format as specified by PKCS#7.
- The operation will resume directly if \(0\).

**10. Exit the operation:** 
- Write to register DS_SET_FINISH_REG, then poll DS_QUERY_BUSY_REG until software reads O.

After completion:
- All input/output registers and memory blocks are cleared for subsequent operations or resets as per system requirements by Espressif Systems (page 902).