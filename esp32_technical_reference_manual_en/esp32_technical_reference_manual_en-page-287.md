**Chapter Title:**
Chapter 15 RSA Accelerator (RSA)

**Section Titles and Content:**

- **15.1 Introduction**
  - The RSA Accelerator provides hardware support for multiple precision arithmetic operations used in RSA asymmetric cipher algorithms.
  - Sometimes, multiple precision arithmetic is also called "bignum arithmetic", "bigit arithmetic" or "arbitrary precision arithmetic".

- **15.2 Features**
  - Support for large-number modular exponentiation
  - Support for large-number modular multiplication
  - Support for large-number multiplication
  - Support for various lengths of operands

- **15.3 Functional Description**

- **15.3.1 Initialization**
  - The RSA Accelerator is activated by enabling the corresponding peripheral clock, and by clearing the DPOR_T_RSA_PD_CTRL_REG register. This releases the RSA Accelerator from reset.
  - When the RSA Accelerator is released from reset, the register RSA_CLEAN_REG reads 0 and an initialization process begins. Hardware initializes the four memory blocks by setting them to 0. After initialization is complete, RSA_CLEAN_REG reads 1. For this reason, software should query RSA_CLEAN_REG after being released from reset, and before writing to any RSA Accelerator memory blocks or registers for the first time.

- **15.3.2 Large Number Modular Exponentiation**
  - Large-number modular exponentiation performs \( Z = X^Y \mod M \). The operation is based on Montgomery multiplication. Aside from the arguments \( X, Y, \) and \( M \), two additional ones are needed — \( T \) and \( M' \). These arguments are calculated in advance by software.
  - The RSA Accelerator supports operand lengths of \( N \in \{512, 1024, 1536, 2048, 2560, 3072, 3584, 4096\} \) bits. The bit length of arguments Z, X, Y, M, and \( T \) can be any one from the N set, but all numbers in a calculation must fit within this range.

**Footer:**
Espressif Systems
287 ESP32 TRM (Version 5.6)
[Submit Documentation Feedback](#)