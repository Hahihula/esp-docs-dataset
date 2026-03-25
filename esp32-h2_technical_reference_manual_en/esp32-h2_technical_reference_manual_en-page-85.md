

```markdown
Chapter 1 ESP-RISC-V CPU

GoBack

1.14.2.3 AMO Instructions

An atomic memory operation (AMO) instruction executes in 3 steps:

1. Read data from the memory address given by rs1, and save it to destination register rd.
2. Combine the data in rd and rs2 according to the operation type and keep the result for Step 3 below.
3. Write the result obtained in Step 2 above to the memory address given by rs1.

There are 9 different AMO operations: SWAP, ADD, AND, OR, XOR, MAX, MIN, MAXU and MINU.

During this whole process, the memory address is kept locked from being accessed by other harts. If a misaligned address is encountered, it will cause an exception with mcause = 6.

For AMO operations both load and store access faults (PMP/PMA) are checked in the 1st step itself. For such cases mcause = 7.
```