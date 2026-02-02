**Chapter Title:**
Chapter 15 RSA Accelerator (RSA)

**Section Titles and Content:**

- **6. Read the result \(Z_i\) (\(i \in [0, n]\) from RSA_Z_MEM.**
  
- **7. Write 1 to RSA_INTERRUPT_REG to clear the interrupt.**

After the operation, the RSAMultModeReg register, memory blocks RSA_Y_MEM and RSA_M_MEM as well as the RSA_M_PRIME_REG will not have changed. However, \(X_i\) in RSA_X_MEM and \(\bar{r}_i\) in RSA_Z_MEM will have been overwritten. In order to perform another operation, refresh the registers and memory blocks, as required.

**15.3.3 Large Number Modular Multiplication**

Large-number modular multiplication performs \(Z = X \times Y \mod M\). This operation is based on Montgomery multiplication. The same values \(\bar{r}\) and \(M'\) are derived by software using the formulas 15.1 and 15.2 shown above.

The RSA Accelerator supports large-number modular multiplication with eight different operand lengths, which are the same as in the large-number modular exponentiation. The operation is performed by a combination of software and hardware. The software performs two hardware operations in sequence.
 
**Software process:**
1. Write \(\frac{N}{512} - 1\) to RSA_MULT_MODE_REG.

2. Write \(X_i, M_i\) (\(i \in [0, n]\)) to registers RSA_X_MEM, RSA_M_MEM and RSA_Z_MEM. Write data to each memory block only according to the length of the number. Data beyond this length are ignored.
   
3. Write \(M'\) to RSA_M_PRIME_REG.

4. Write 1 to RSA_MULT_START_REG.

5. Wait for the first round of the operation to be completed. Poll RSA_INTERRUPT_REG until it reads 1, or until the RSA_INTR interrupt is generated.

6. Write 1 to RSA_INTERRUPT_REG to clear the interrupt.
   
7. Write \(Y_i\) (\(i \in [0, n]\)) to RSA_X_MEM.

Users need to write to the memory block only according to the length of the number. Data beyond this length are ignored.

8. Write 1 to RSA_MULT_START_REG.

9. Wait for the second round of the operation to be completed. Poll RSA_INTERRUPT_REG until it reads 1, or until the RSA_INTR interrupt is generated.
   
10. Read the result \(Z_i\) (\(i \in [0, n]\)) from RSA_Z_MEM.

11. Write 1 to RSA_INTERRUPT_REG to clear the interrupt.

After the operation, the RSA_MULT_MODE_REG register, and memory blocks RSA_M_MEM and RSA_M_PRIME_REG remain unchanged. Users do not need to refresh these registers or memory blocks if the values remain the same.
 
**15.3.4 Large Number Multiplication**

Large-number multiplication performs \(Z = X \times Y\). The length of Z is twice that of X and Y. Therefore, the RSA Accelerator supports large-number multiplication with only four operand lengths.

**Footer:**
Espressif Systems
289 ESP32 TRM (Version 5.6)
Submit Documentation Feedback