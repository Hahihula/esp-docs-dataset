
```markdown
Chapter 27 Digital Signature Algorithm (DSA)

the hardware steps described in Section 27.3.4.

We assume that the software has called the HMAC peripheral and the HMAC peripheral has calculated DSA_KEY based on HMAC_KEY.

1. Prerequisites: Prepare operands C, X, IV according to Section 27.3.3.
2. Activate the DSA peripheral: Write 1 to DS_SET_START_REG.
3. Check if DSA_KEY is ready depending on from where the DSA_KEY comes from:

   - Write 1 to DS_KEY_SOURCE_REG to select the DSA_KEY deployed by the Key Manager. Verify that DSA_KEY has been successfully deployed by checking the register field KEYMNG_KEY_DS_VLD. When its value is 1, it indicates that DSA_KEY has been successfully deployed and is ready.
   
   - Write 0 to DS_KEY_SOURCE_REG to select the DSA_KEY from HMAC. Poll DS_QUERY_BUSY_REG until the software reads 0.

If the software does not read 0 in DS_QUERY_BUSY_REG after approximately 1 ms, it indicates a problem with HMAC initialization. In such a case, the software can read register DS_QUERY_KEY_WRONG_REG to get more information:

   - If the software reads 0 in DS_QUERY_KEY_WRONG_REG, it indicates that the HMAC peripheral has not been called.
   
   - If the software reads any value from 1 to 15 in DS_QUERY_KEY_WRONG_REG, it indicates that HMAC was called, but the DSA module did not successfully get the DSA_KEY value from the HMAC peripheral. This may indicate that the HMAC operation has been interrupted due to a software concurrency problem.

4. Write IV to memory block DS_IV_MEM: Write the content in the IV block to the memory block DS_IV_MEM, which is 16 bytes. For more information on the IV block, please refer to Chapter 22 AES Accelerator (AES).

5. Write X to memory block DS_X_MEM: Write Xi (i ∈ {0,1,...,n−1}), where n = N/32, to memory block DS_X_MEM whose capacity is 96 words. Each word can store one base-b digit. The memory block uses the little endian format for storage, i.e., the least significant digit of the operand is in the lowest address. Words in DS_X_MEM block after the configured length of X (N bits, as described in Section 27.3.2), are ignored.

6. Write C to corresponding memory blocks: Write the four sub-parameters of C to corresponding memory blocks:

   - Write Yi (i ∈ {0,1,...,95}) to DS_Y_MEM.
   
   - Write Mi (i ∈ {0,1,...,95}) to DS_M_MEM.
   
   - Write ri (i ∈ {0,1,...,95}) to DS_RB_MEM.
   
   - write Boxi (i ∈ {0,1,...,11}) to DS_BOX_MEM.

The capacity of DS_Y_MEM, DS_M_MEM, and DS_RB_MEM is 96 words, whereas the capacity of DS_BOX_MEM is only 12 words. Each word can store one base-b digit. The memory blocks use the little endian format for storage, i.e., the least significant digit of the operand is in the lowest address.

7. Start DSA operation: Write 1 to register DS_SET_CONTINUE_REG.
```