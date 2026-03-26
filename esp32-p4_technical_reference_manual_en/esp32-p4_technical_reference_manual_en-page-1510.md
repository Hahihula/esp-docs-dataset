

```markdown
Chapter 30 RSA Digital Signature Peripheral (RSA_DS)

the hardware steps described in Section 30.3.4.

We assume that the software has called the HMAC peripheral and the HMAC peripheral has calculated `RSA_DS_KEY` based on `HMAC_KEY`.

1. Prerequisites: Prepare operands C, X, IV according to Section 30.3.3.
2. Activate the RSA_DS peripheral: Write 1 to DSA_SET_START_REG.
3. Check if `RSA_DS_KEY` is ready depending on from where the `RSA_DS_KEY` comes from:

   - Write 1 to `DSA_KEY_SOURCE_REG` to select `RSA_DS_KEY` deployed by the Key Manager. Verify that `RSA_DS_KEY` has been successfully deployed by checking the register field `KEYMNG_KEY_DS_VLD`. When its value is 1, it indicates that `RSA_DS_KEY` has been successfully deployed and is ready.
   - Write 0 to `DSA_KEY_SOURCE_REG` to select `RSA_DS_KEY` from HMAC. Poll `DSA_QUERY_BUSY_REG` until the software reads 0.

If the software does not read 0 in `DSA_QUERY_BUSY_REG` after approximately 1 ms, it indicates a problem with HMAC initialization. In such a case, the software can read register `DSA_QUERY_KEY_WRONG_REG` to get more information:

   - If the software reads 0 in `DSA_QUERY_KEY_WRONG_REG`, it indicates that the HMAC peripheral has not been called.
   - If the software reads any value from 1 to 15 in `DSA_QUERY_KEY_WRONG_REG`, it indicates that HMAC was called, but the RSA_DS peripheral did not successfully get `RSA_DS_KEY` from the HMAC peripheral. This may indicate that the HMAC operation has been interrupted due to a software concurrency problem.

4. Configure register: Write the content in the IV block to register DSA_IV_m_REG (m: 0 ~ 3). For more information on the IV block, please refer to Chapter 25 AES Accelerator (AES).

5. Write X to memory block DSA_X_MEM: Write `X_i` (`i ∈ {0,1,...,n−1}`), where `n = N/32`, to memory block `DSA_X_MEM` whose capacity is 96 words. Each word can store one base-b digit. The memory block uses the little endian format for storage, i.e., the least significant digit of the operand is in the lowest address. Words in `DSA_X_MEM` block after the configured length of X (`N` bits, as described in Section 30.3.2), are ignored.

6. Write C to corresponding memory blocks: Write the four sub-parameters of C to corresponding memory blocks:

   - Write `Ŷ_i` (`i ∈ {0,1,...,127}`) to DSA_Y_MEM.
   - Write `M̂_i` (`i ∈ {0,1,...,127}`) to DSA_M_MEM.
   - Write `r̂_i` (`i ∈ {0,1,...,127}`) to DSA_RB_MEM.
   - write `B̂ox_i` (`i ∈ {0,1,...,11}`) to DSA_BOX_MEM.

The capacity of `DSA_Y_MEM`, `DSA_M_MEM`, and `DSA_RB_MEM` is 128 words, whereas the capacity of `DSA_BOX_MEM` is only 12 words. Each word can store one base-b digit. The memory blocks use the little endian format for storage, i.e., the least significant digit of the operand is in the lowest address.

7. Start RSA_DS operation: Write 1 to register DSA_SET_ME_REG.
```