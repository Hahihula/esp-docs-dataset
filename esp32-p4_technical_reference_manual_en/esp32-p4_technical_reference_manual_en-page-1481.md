
```markdown
(b) Write M′ to the RSA_M_PRIME_REG register.

(c) Configure registers related to the acceleration options, which are described later in Section 28.3.5.

3. Write Xi, Yi, Mi and ri for i ∈ {0,1,...,n−1} to memory blocks RSA_X_MEM, RSA_Y_MEM, RSA_M_MEM and RSA_Z_MEM. The capacity of each memory block is 128 words. Each word of each memory block can store one base-b digit. The memory blocks use the little endian format for storage, i.e., the least significant digit of each number is in the lowest address.

Users need to write data to each memory block only according to the length of the number; data beyond this length is ignored.

4. Write 1 to the RSA_SET_START_MODEXP field of the RSA_SET_START_MODEXP_REG register to start computation.

5. Wait for the completion of computation, which happens when the content of RSA_QUERY_IDLE becomes 1 or the RSA interrupt occurs, if enabled.

6. Read the result Zi for i ∈ {0,1,...,n−1} from RSA_Z_MEM.

7. If you have the interrupt enabled, write 1 to RSA_CLEAR_INTERRUPT to clear the interrupt.
```

```markdown
After the computation, the RSA_MODE_REG register, memory blocks RSA_Y_MEM and RSA_M_MEM, as well as the RSA_M_PRIME_REG remain unchanged. However, Xi in RSA_X_MEM and ri in RSA_Z_MEM computation are overwritten, and only these overwritten memory blocks need to be re-initialized before starting another computation.
```

```markdown
## 28.3.3 Large-Number Modular Multiplication

Large-number modular multiplication performs Z = X × Y mod M. This computation is based on Montgomery multiplication. Therefore, similar to the large-number modular exponentiation, two additional arguments are needed – r̄ and M′, which need to be calculated in advance by software.

The RSA accelerator supports large-number modular multiplication with operands of length N = 32 × n, where n ∈ {1,2,3,...,128}.
```

```markdown
The computation can be executed as follows:

1. Write 1 or 0 to the RSA_INT_ENA_REG register to enable or disable the interrupt function.

2. Configure relevant configuration registers:

   (a) Write (N/32 − 1) to the RSA_MODE_REG register.

   (b) Write M′ to the RSA_M_PRIME_REG register.

3. Write Xi, Yi, Mi, and ri for i ∈ {0,1,...,n−1} to memory blocks RSA_X_MEM, RSA_Y_MEM, RSA_M_MEM, and RSA_Z_MEM, respectively. The capacity of each memory block is 128 words. Each word of each memory block can store one base-b digit. The memory blocks use the little endian format for storage, i.e., the least significant digit of each number is in the lowest address.

Users need to write data to each memory block only according to the length of the number; data beyond this length are ignored.

4. Write 1 to the RSA_SET_START_MODMULT field.
```