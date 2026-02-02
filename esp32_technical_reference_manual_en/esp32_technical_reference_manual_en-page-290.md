**Chapter Title:**
Chapter 15 RSA Accelerator (RSA)

**Body Text with Equations and Instructions:**

The length \( \hat{N} \) of the result Z is defined as:
\[ N = {512, 1024, 1536, 2048} \text{ bits.} \]

Operands X and Y need to be extended to form arguments \( \hat{X} \) and \( \hat{Y} \), which have the same length (N bits). The result Z is left-extended.

\[ 
\hat{X} = (\hat{X}_{n-1}\hat{X}_{n-2} \cdots \hat{X}_0)_b \\
\hat{Y} = (\hat{Y}_{n-1}\hat{Y}_{n-2} \cdots \hat{Y}_0)_b 
\]

where:
\[ n = \frac{N}{32} \]
\[ \hat{N} = 2 \times N \]
\[ i = \frac{\hat{N}}{32} = 2n \]

Software performs the operation in this order:

1. Write \( (\frac{\hat{N}}{2} + 8) \) to RSA_MULT_MODE_REG.
2. Write \( X_i \) and \( Y_i \) (i ∈ [0, n]) to RSA_X_MEM and RSA_Z_MEM respectively.

Write the valid data into each number's memory block according to their lengths. Values beyond this length are ignored. Half of the base-b positional notations written in zero using derivations shown above). These zero values is indispensable.
3. Write 1 to RSA_MULT_START_REG.
4. Wait for the operation to be completed. Poll RSA_INTERRUPT_REG until it reads 1, or until the RSA_INSTR interrupt is generated.

Read the result \( Z_i \) (i ∈ [0, n]) from RSA_Z_MEM and write back into memory block corresponding positions in zero padding as necessary before writing data.
6. Write 1 to RSA_INTERRUPT_REG to clear the interrupt after operation only RSA_MULT_MODE_REG register remains unmodified

**Section Title:**
15.4 Register Summary

**Table of Registers with Descriptions, Addresses (in hexadecimal), and Access Types**

| Name                          | Description                                    | Address       | Access |
|-------------------------------|-----------------------------------------------|--------------|--------|
| Configuration registers        |                                               |              |        |
| RSA_M_PRIME_REG               | Register to store M'                           | 0x3FF02800   | R/W    |
| Modular exponentiation registers |                   |                |        |
| RSA_MODEXP_MODE_REG          | Modular exponentiation mode                    | 0x3FF02804   | R/W    |
| RSA_MODEXP_START_REG         | Start bit                                      | 0x3FF02808   | WO     |
| Modular multiplication registers |                   |                |        |
| RSA_MULT_MODE_REG            | Modular multiplication mode                    | 0x3FF0280C   | R/W    |
| RSA_MULT_START_REG           | Start bit                                      | 0x3FF02810   | WO     |
| Misc registers                 |                   |                |        |
| RSA_INTERRUPT_REG             | RSA interrupt register                          | 0x3FF02814   | R/W    |
| RSA_CLEAN_REG                 | RSA clean register                              | 0x3FF02818   | RO     |

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback