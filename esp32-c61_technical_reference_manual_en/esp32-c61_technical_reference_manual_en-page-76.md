

```markdown
# 1.6.5 Atomic (A) Extension

## 1.6.5.1 Overview

Support for atomic (A) extension is available in compliance with RISC-V Instruction Set Manual, Volume I: RISC-V User-Level ISA, Version 2.2, with an emphasis to guarantee forward progress, i.e. any situation that may cause data memory lock for an indefinite amount of time is prevented by their very functionality.

## 1.6.5.2 Functional Description

Atomic (A) Extension contains instructions that atomically read-modify-write memory to support synchronization between multiple RISC-V harts running in the same memory space. The two forms of atomic instruction provided are load-reserved/store-conditional instructions and atomic fetch-and-op memory instructions. The atomic instructions currently ignore the aq (acquire) and rl (release) bits as they are irrelevant to the current architecture, in which memory ordering is always guaranteed.

## 1.6.5.3 Load-Reserve (LR.W) Instruction

The LR.W instruction simply locks a 32-bit aligned memory address to which the load access is being performed. Once a 4-byte memory region is locked, it will remain locked, i.e. other harts won’t be able to access this same memory location, until any of the following scenarios is encountered during execution:

- any load operation
- any store operation
- any interrupts/exceptions
- backward jump/taken backward branch
- JALR
- ECALL/EBREAK/MRET/URET
- FENCE/FENCE.I
- debug mode
- critical section exceeding 64 bytes
- data address in SC.W instruction not matching that in LR.W instruction

If any of the above happens, except SC.W, the memory lock will be released immediately. If an SC instruction is encountered instead, the lock will be released eventually (not immediately) in the manner described in Section 1.6.5.4.

If a misaligned address is encountered, it will cause an exception with `mcause = 6`.

## 1.6.5.4 Store-Conditional (SC.W) Instruction

The SC.W instruction first checks if the memory lock is still valid, and the address is the same as specified during the last LR.W instruction. If so, only then will it perform the store to memory, and later release the lock as soon as it gets an acknowledgement of operation completion from the memory.
```