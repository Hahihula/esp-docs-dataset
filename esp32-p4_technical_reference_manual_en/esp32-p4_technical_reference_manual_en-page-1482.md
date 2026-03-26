

```markdown
5. Wait for the completion of computation, which happens when the content of RSA_QUERY_IDLE becomes 1 or the RSA interrupt occurs, if enabled.
6. Read the result Zᵢ for i ∈ {0, 1, ..., n−1} from RSA_Z_MEM.
7. If you have the interrupt enabled, write 1 to RSA_CLEAR_INTERRUPT to clear the interrupt.

After the computation, the length of operands in RSA_MODE_REG, the Xᵢ in memory RSA_X_MEM, the Yᵢ in memory RSA_Y_MEM, the Mᵢ in memory RSA_M_MEM, and the M' in memory RSA_M_PRIME_REG remain unchanged. However, the r̄ᵢ in memory RSA_Z_MEM has already been overwritten, and only this overwritten memory block needs to be re-initialized before starting another computation.

## 28.3.4 Large-Number Multiplication

Large-number multiplication performs Z = X × Y. The length of result Z is twice that of operand X and operand Y. Therefore, the RSA accelerator only supports large-number multiplication with operand length N = 32 × n, where n ∈ {1, 2, 3, ..., 64}. The length Ė of result Z is 2 × N.

The computation can be executed as follows:

1. Write 1 or 0 to the RSA_INT_ENA_REG register to enable or disable the interrupt function.
2. Write (N/32 − 1), i.e., ((N/16) − 1) to the RSA_MODE_REG register.
3. Write Xᵢ and Yᵢ for ∈ {0, 1, ..., n−1} to memory blocks RSA_X_MEM and RSA_Z_MEM. Each word of each memory block can store one base-b digit. The memory blocks use the little endian format for storage, i.e., the least significant digit of each number is in the lowest address. n is N/32.
   Write Xᵢ for i ∈ {0, 1, ..., n−1} to the address of the i words of the RSA_X_MEM memory block. Note that Yᵢ for i ∈ {0, 1, ..., n−1} will not be written to the address of the i words of the RSA_Z_MEM register, but the address of the n + i words, i.e., the base address of the RSA_Z_MEM memory plus the address offset 4 × (n + i).

Users need to write data to each memory block only according to the length of the number; data beyond this length is ignored.

4. Write 1 to the RSA_SET_START_MULT register.
5. Wait for the completion of computation, which happens when the content of RSA_QUERY_IDLE becomes 1 or the RSA interrupt occurs, if enabled.
6. Read the result Zᵢ for i ∈ {0, 1, ..., n−1} from the RSA_Z_MEM register. Ė is 2 × n.
7. If you have the interrupt enabled, write 1 to RSA_CLEAR_INTERRUPT to clear the interrupt.

After the computation, the length of operands in RSA_MODE_REG and the Xᵢ in memory RSA_X_MEM remain unchanged. However, the Yᵢ in memory RSA_Z_MEM has already been overwritten, and only this overwritten memory block needs to be re-initialized before starting another computation.

## 28.3.5 Options for Additional Acceleration

The ESP32-P4 RSA accelerator also provides SEARCH and CONSTANT_TIME options that can be configured to further accelerate the large-number modular exponentiation. By default, both options are configured as no additional acceleration.
```