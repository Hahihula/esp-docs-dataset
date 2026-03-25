

```markdown
8. Wait for the operation to be completed: Poll register DS_QUERY_BUSY_REG until the software reads 0.
9. Query check result: Read register DS_QUERY_CHECK_REG and conduct subsequent operations as illustrated below based on the return value:
    * If the value is 0, it indicates that both the padding check and MD check pass. Users can continue to get the signed result Z.
    * If the value is 1, it indicates that the padding check passes but MD check fails. The signed result Z is invalid. The operation will resume directly from Step 11.
    * If the value is 2, it indicates that the padding check fails but the MD check passes. Users can continue to get the signed result Z. But please note that the data does not comply with the aforementioned PKCS#7 padding format, which may not be what you want.
    * If the value is 3, it indicates that both the padding check and MD check fail. In this case, some fatal errors have occurred and the signed result Z is invalid. The operation will resume directly from Step 11.
10. Read the signed result: Read the signed result Zi (i ∈ {0, 1, ..., n−1}), where n = N/32, from memory block DS_Z_MEM. The memory block stores Z in little-endian byte order.
11. Exit the operation: Write 1 to DS_SET_FINISH_REG, and then poll DS_QUERY_BUSY_REG until the software reads 0.

After the operation, all the input/output registers and memory blocks are cleared.
```