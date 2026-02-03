**Chapter Title:**
Chapter 20 RSA Accelerator (RSA)

**Section Header and Content:**

3. Write \(X_i, Y_i, M_i\) and \(\bar{r}_i\) for \(i \in {0,1,\ldots,n-1}\) to memory blocks `RSA_X_MEM`, `RSA_Y_MEM`, `RSA_M_MEM` and `RSA_Z_MEM`. The capacity of each memory block is 128 words. Each word of each memory block can store on the base-\(b\) digit. The memory blocks use the little endian format for storage, i.e., the least significant digit of each number is in the lowest address.

Users need to write data to each memory block only according to the length of the number; data beyond this length are ignored.

4. Write 1 to `RSA_MODEXP_START_REG` register to start computation.
5. Wait for the completion of computation, which happens when the content of `RSA_IDLE_REG` becomes 1 or the RSA interrupt occurs.
6. Read the result \(Z_i\) for \(i \in {0,1,\ldots,n-1}\) from `RSA_Z_MEM`.
7. Write 1 to `RSA_CLEAR_INTERRUPT_REG` to clear the interrupt, if you have enabled the interrupt function.

After the computation, the `RSA_MODE_REG` register, memory blocks `RSA_Y_MEM` and `RSA_M_MEM`, as well as the `RSA_M_PRIME_REG` remain unchanged. However, \(X_i\) in `RSA_X_MEM` and \(\bar{r}_i\) in `RSA_Z_MEM` are overwritten; only these overwritten memory blocks need to be re-initialized before starting another computation.

**Subsection Title:**
20.3.2 Large Number Modular Multiplication

**Body Text of Subsection 20.3.2**

Large-number modular multiplication performs \(Z = X \times Y\) mod \(M\). This computation is based on Montgomery multiplication. Therefore, similar to the large number modular exponentiation, two additional arguments are needed – \(\bar{r}\) and \(M'\), which need to be calculated in advance by software.

The RSA Accelerator supports large-number modular multiplication with operands of 128 different lengths.

**List under Subsection Title:**
- The computation can be executed as follows:
  - Write 1 or 0 to the `RSA_INTERRUPT_ENA_REG` register to enable or disable the interrupt function.
  - Configure relevant registers:

    (a) Write \(\left\lfloor \frac{N}{32} \right\rfloor\) – 1 to the `RSA_MODE_REG` register.

  - Write \(M'\) to the `RSA_M_PRIME_REG` register. 

- Write \(X_i, Y_i, M_i,\) and \(\bar{r}_i\) for \(i \in {0,1,\ldots,n-1}\) to memory blocks `RSA_X_MEM`, `RSA_Y_MEM`, `RSA_M_MEM` and `RSA_Z_MEM`. The capacity of each memory block is 128 words. Each word of each memory block can store on the base-\(b\) digit. The memory blocks use the little endian format for storage, i.e., the least significant digit of each number is in the lowest address.

Users need to write data to each memory block only according to the length of the number; data beyond this length are ignored.
4. Write 1 to `RSA_MODMULT_START_REG` register.
5. Wait for the completion of computation, which happens when the content of `RSA_IDLE_REG` becomes 1 or the RSA interrupt occurs.

6. Read the result \(Z_i\) for \(i \in {0,1,\ldots,n-1}\) from `RSA_Z_MEM`.
7. Write 1 to `RSA_CLEAR_INTERRUPT_REG` to clear the interrupt, if you have enabled the interrupt function.
  
**Footer:**
Espressif Systems
875 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback