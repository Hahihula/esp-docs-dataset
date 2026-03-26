

```markdown
On the other hand, if the lock is found to have been invalidated (due to any of the situations as described in Section 1.6.6.3), it will set a fail code (currently always 1) in the destination register rd.

If a misaligned address is encountered, it will cause an exception with `mcause = 6`.

### 1.6.6.5 AMO Instructions

An AMO instruction executes in three steps:

1. Read data from memory address given by rs1, and save it to destination register rd.
2. Combine the data in rd and rs2 according to the operation type and keep the result for Step 3 below.
3. Write the result obtained in Step 2 above to memory address given by rs1.

There are nine different AMO operations: SWAP, ADD, AND, OR, XOR, MAX, MIN, MAXU, and MINU.

During this whole process, the memory address is kept locked from being accessed by other harts. If a misaligned address is encountered, it will cause an exception with `mcause = 6`.

For AMO operations both load and store access faults (PMP/PMA) are checked in the 1st step itself. For such cases `mcause = 7`.
```