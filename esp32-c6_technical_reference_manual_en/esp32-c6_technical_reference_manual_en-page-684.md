

```markdown
Users need to write data to each memory block only according to the length of the number; data beyond this length is ignored.

4. Write 1 to the RSA_SET_START_MODEXP field of the RSA_SET_START_MODEXP_REG register to start computation.

5. Wait for the completion of computation, which happens when the content of RSA_QUERY_IDLE becomes 1 or the RSA interrupt occurs.

6. Read the result Z_i for i ∈ {0, 1, ..., n−1} from RSA_Z_MEM.

7. Write 1 to RSA_CLEAR_INTERRUPT to clear the interrupt, if you have the interrupt enabled.
```

```markdown
After the computation, the RSA_MODE_REG register, memory blocks RSA_Y_MEM and RSA_M_MEM, as well as the RSA_M_PRIME_REG remain unchanged. However, X_i in RSA_X_MEM and r̄_i in RSA_Z_MEM computation are overwritten, and only these overwritten memory blocks need to be re-initialized before starting another computation.
```

## 22.3.2 Large-number Modular Multiplication

Large-number modular multiplication performs Z = X × Y mod M. This computation is based on Montgomery multiplication. Therefore, similar to the large-number modular exponentiation, two additional arguments are needed — r̄ and M', which need to be calculated in advance by software.

The RSA accelerator supports large-number modular multiplication with operands of 96 different lengths.

The computation can be executed as follows:

1. Write 1 or 0 to the RSA_INT_ENA_REG register to enable or disable the interrupt function.

2. Configure relevant registers:
   (a) Write (N/32 − 1) to the RSA_MODE_REG register.
   (b) Write M' to the RSA_M_PRIME_REG register.

3. Write X_i, Y_i, M_i, and r̄_i for i ∈ {0, 1, ..., n−1} to memory blocks RSA_X_MEM, RSA_Y_MEM, RSA_M_MEM, and RSA_Z_MEM, respectively. The capacity of each memory block is 96 words. Each word of each memory block can store one base-b digit. The memory blocks use the little endian format for storage, i.e., the least significant digit of each number is in the lowest address.

Users need to write data to each memory block only according to the length of the number; data beyond this length are ignored.

4. Write 1 to the RSA_SET_START_MODMULT field.

5. Wait for the completion of computation, which happens when the content of RSA_QUERY_IDLE becomes 1 or the RSA interrupt occurs.

6. Read the result Z_i for i ∈ {0, 1, ..., n−1} from RSA_Z_MEM.

7. Write 1 to RSA_CLEAR_INTERRUPT to clear the interrupt, if you have the interrupt enabled.

After the computation, the length of operands in RSA_MODE_REG, the X_i in memory RSA_X_MEM, the Y_i in memory RSA_Y_MEM, the M_i in memory RSA_M_MEM, and the M' in memory RSA_M_PRIME_REG remain
```