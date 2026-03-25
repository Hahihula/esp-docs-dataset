

```markdown
3. Check if `DSA_KEY` is ready: Poll `DS_QUERY_BUSY_REG` until the software reads 0.

If the software does not read 0 in `DS_QUERY_BUSY_REG` after approximately 1 ms, it indicates a problem with HMAC initialization. In such a case, the software can read register `DS_QUERY_KEY_WRONG_REG` to get more information:

* If the software reads 0 in `DS_QUERY_KEY_WRONG_REG`, it indicates that the HMAC peripheral has not been called.
* If the software reads any value from 1 to 15 in `DS_QUERY_KEY_WRONG_REG`, it indicates that HMAC was called, but the DSA module did not successfully get the `DSA_KEY` value from the HMAC peripheral. This may indicate that the HMAC operation has been interrupted due to a software concurrency problem.

4. Configure register: Write the content in the `IV` block to register `DS_IV_m_REG` (`m`: 0 ~ 3). For more information on the `IV` block, please refer to Chapter 19 AES Accelerator (AES).

5. Write `X` to memory block DS_X_MEM: Write `Xi` (`i ∈ {0,1,...,n−1}`), where `n = N/32`, to memory block `DS_X_MEM` whose capacity is 96 words. Each word can store one base-b digit. The memory block uses the little endian format for storage, i.e., the least significant digit of the operand is in the lowest address. Words in `DS_X_MEM` block after the configured length of `X` (`N` bits, as described in Section 24.3.2), are ignored.

6. Write `C` to corresponding memory blocks: Write the four sub-parameters of `C` to corresponding memory blocks:

* Write `Yi` (`i ∈ {0,1,...,95}`) to `DS_Y_MEM`.
* Write `Mi` (`i ∈ {0,1,...,95}`) to `DS_M_MEM`.
* Write `Ri` (`i ∈ {0,1,...,95}`) to `DS_RB_MEM`.
* write `Boxi` (`i ∈ {0,1,...,11}`) to `DS_BOX_MEM`.

The capacity of `DS_Y_MEM`, `DS_M_MEM`, and `DS_RB_MEM` is 96 words, whereas the capacity of `DS_BOX_MEM` is only 12 words. Each word can store one base-b digit. The memory blocks use the little endian format for storage, i.e., the least significant digit of the operand is in the lowest address.

7. Start DSA operation: Write 1 to register `DS_SET_ME_REG`.

8. Wait for the operation to be completed: Poll register `DS_QUERY_BUSY_REG` until the software reads 0.

9. Query check result: Read register `DS_QUERY_CHECK_REG` and conduct subsequent operations as illustrated below based on the return value:

* If the value is 0, it indicates that both the padding check and MD check pass. Users can continue to get the signed result Z.
* If the value is 1, it indicates that the padding check passes but MD check fails. The signed result Z is invalid. The operation will resume directly from Step 11.
* If the value is 2, it indicates that the padding check fails but the MD check passes. Users can continue to get the signed result Z. But please note that the data does not comply with the aforementioned PKCS#7 padding format, which may not be what you want.
* If the value is 3, it indicates that both the padding check and MD check fail. In this case, some fatal errors have occurred and the signed result Z is invalid. The operation will resume directly from Step
```