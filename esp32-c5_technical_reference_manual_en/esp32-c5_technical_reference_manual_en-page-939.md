

# 27.4 Memory Summary

The addresses in this section are relative to the Digital Signature Algorithm base address provided in Table 6.3-2 in Chapter 6 System and Memory.

| Name        | Description             | Size (byte) | Starting Address | Ending Address | Access |
|-------------|-------------------------|-----------|------------------|----------------|--------|
| DS_Y_MEM    | Memory block Y          | 512       | 0x0000           | 0x01FF         | R/W    |
| DS_M_MEM    | Memory block M          | 512       | 0x0200           | 0x03FF         | R/W    |
| DS_RB_MEM   | Memory block τ          | 512       | 0x0400           | 0x05FF         | R/W    |
| DS_BOX_MEM  | Memory block Box        | 48        | 0x0600           | 0x062F         | R/W    |
| DS_IV_MEM   | Memory block IV         | 16        | 0x0630           | 0x063F         | R/W    |
| DS_X_MEM    | Memory block X          | 512       | 0x0800           | 0x09FF         | R/W    |
| DS_Z_MEM    | Memory block Z          | 512       | 0x0A00           | 0x0BFF         | R/W    |