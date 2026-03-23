

```markdown
| Name              | Description       | Size (byte) | Starting Address | Ending Address | Access |
|-------------------|-------------------|-------------|------------------|----------------|--------|
| RSA_M_MEM         | Memory M          | 384         | 0x0000           | 0x017F         | R/W    |
| RSA_Z_MEM         | Memory Z          | 384         | 0x0200           | 0x037F         | R/W    |
| RSA_Y_MEM         | Memory Y          | 384         | 0x0400           | 0x057F         | R/W    |
| RSA_X_MEM         | Memory X          | 384         | 0x0600           | 0x077F         | R/W    |

## 22.5 Register Summary

The addresses in this section are relative to the RSA accelerator base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                      | Description                                                                 | Address   | Access |
|-------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| **Control / Configuration Registers**     |                                                                             |           |        |
| RSA_M_PRIME_REG                           | Represents M'                                                               | 0x0800    | R/W    |
| RSA_MODE_REG                              | Configures RSA length                                                      | 0x0804    | R/W    |
| RSA_SET_START_MODEXP_REG                  | Starts modular exponentiation                                               | 0x080C    | WT     |
| RSA_SET_START_MODMULT_REG                 | Starts modular multiplication                                                | 0x0810    | WT     |
| RSA_SET_START_MULT_REG                    | Starts multiplication                                                        | 0x0814    | WT     |
| RSA_QUERY_IDLE_REG                        | Represents the RSA status                                                   | 0x0818    | RO     |
| RSA_CONSTANT_TIME_REG                     | Configures the constant_time option                                         | 0x0820    | R/W    |
| RSA_SEARCH_ENABLE_REG                     | Configures the search option                                                 | 0x0824    | R/W    |
| RSA_SEARCH_POS_REG                        | Configures the search position                                               | 0x0828    | R/W    |
| **Status Register**                       |                                                                             |           |        |
| RSA_QUERY_CLEAN_REG                       | RSA initialization status                                                    | 0x0808    | RO     |
| **Interrupt Registers**                   |                                                                             |           |        |
| RSA_INT_CLR_REG                            | Clears RSA interrupt                                                         | 0x081C    | WT     |
| RSA_INT_ENA_REG                            | Enables the RSA interrupt                                                    | 0x082C    | R/W    |
| **Version Control Register**              |                                                                             |           |        |
| RSA_DATE_REG                               | Version control register                                                     | 0x0830    | R/W    |
```