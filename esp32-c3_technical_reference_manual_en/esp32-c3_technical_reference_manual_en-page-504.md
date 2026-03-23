

```markdown
(c) Configure registers related to the acceleration options, which are described later in Section 20.3.4.

3. Write $X_i$, $Y_i$, $M_i$ and $\bar{r}_i$ for $i \in \{0,1,\dots,n-1\}$ to memory blocks RSA_X_MEM, RSA_Y_MEM, RSA_M_MEM and RSA_Z_MEM. The capacity of each memory block is 96 words. Each word of each memory block can store one base-$b$ digit. The memory blocks use the little endian format for storage, i.e. the least significant digit of each number is in the lowest address.

Users need to write data to each memory block only according to the length of the number; data beyond this length are ignored.

4. Write 1 to the RSA_MODEXP_START_REG register to start computation.

5. Wait for the completion of computation, which happens when the content of RSA_IDLE_REG becomes 1 or the RSA interrupt occurs.

6. Read the result $Z_i$ for $i \in \{0,1,\dots,n-1\}$ from RSA_Z_MEM.

7. Write 1 to RSA_CLEAR_INTERRUPT_REG to clear the interrupt, if you have enabled the interrupt function.

After the computation, the RSA_MODE_REG register, memory blocks RSA_Y_MEM and RSA_M_MEM, as well as the RSA_M_PRIME_REG remain unchanged. However, $X_i$ in RSA_X_MEM and $\bar{r}_i$ in RSA_Z_MEM computation are overwritten, and only these overwritten memory blocks need to be re-initialized before starting another computation.

## 20.3.2 Large Number Modular Multiplication

Large-number modular multiplication performs $Z = X \times Y \bmod M$. This computation is based on Montgomery multiplication. Therefore, similar to the large number modular exponentiation, two additional arguments are needed — $\bar{r}$ and $M'$, which need to be calculated in advance by software.

The RSA Accelerator supports large-number modular multiplication with operands of 96 different lengths.

The computation can be executed as follows:

1. Write 1 or 0 to the RSA_INTERRUPT_ENA_REG register to enable or disable the interrupt function.

2. Configure relevant registers:

   (a) Write $(\frac{N}{32} - 1)$ to the RSA_MODE_REG register.

   (b) Write $M'$ to the RSA_M_PRIME_REG register.

3. Write $X_i$, $Y_i$, $M_i$, and $\bar{r}_i$ for $i \in \{0,1,\dots,n-1\}$ to memory blocks RSA_X_MEM, RSA_Y_MEM, RSA_M_MEM and RSA_Z_MEM. The capacity of each memory block is 96 words. Each word of each memory block can store one base-$b$ digit. The memory blocks use the little endian format for storage, i.e. the least significant digit of each number is in the lowest address.

Users need to write data to each memory block only according to the length of the number; data beyond this length are ignored.

4. Write 1 to the RSA_MODMULT_START_REG register.

5. Wait for the completion of computation, which happens when the content of RSA_IDLE_REG becomes 1 or the RSA interrupt occurs.

6. Read the result $Z_i$ for $i \in \{0,1,\dots,n-1\}$ from RSA_Z_MEM.
```