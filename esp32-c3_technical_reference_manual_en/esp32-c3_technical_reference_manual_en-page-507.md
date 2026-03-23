

# 20.4 Memory Summary

The addresses in this section are relative to the RSA accelerator base address provided in Table 3.3-3 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

Table 20.4-1. RSA Accelerator Memory Blocks

| Name          | Description | Size (byte) | Starting Address | Ending Address | Access |
|---------------|-------------|-------------|------------------|----------------|--------|
| RSA_M_MEM     | Memory M    | 384         | 0x0000           | 0x017F         | R/W    |
| RSA_Z_MEM     | Memory Z    | 384         | 0x0200           | 0x037F         | R/W    |
| RSA_Y_MEM     | Memory Y    | 384         | 0x0400           | 0x057F         | R/W    |
| RSA_X_MEM     | Memory X    | 384         | 0x0600           | 0x077F         | R/W    |