

# 30.4 Memory Summary

The addresses in this section are relative to the RSA Digital Signature Peripheral (RSA_DS) base address provided in Table 7.3-2 in Chapter 7 System and Memory.

| Name         | Description     | Size (byte) | Starting Address | Ending Address | Access |
|--------------|-----------------|-------------|------------------|----------------|--------|
| DSA_Y_MEM    | Memory block Y  | 512         | 0x0000           | 0x01FF        | WO     |
| DSA_M_MEM    | Memory block M  | 512         | 0x0200           | 0x03FF        | WO     |
| DSA_RB_MEM   | Memory block r̄ | 512         | 0x0400           | 0x05FF        | WO     |
| DSA_BOX_MEM  | Memory block Box| 48          | 0x0600           | 0x062F        | WO     |
| DSA_X_MEM    | Memory block X  | 512         | 0x0800           | 0x09FF        | WO     |
| DSA_Z_MEM    | Memory block Z  | 512         | 0x0A00           | 0x0BFF        | RO     |