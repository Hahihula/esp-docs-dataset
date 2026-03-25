

# 22.6 Memory Blocks

ECDSA's memory blocks store input data and output data of the ECDSA operation.

Table 22.6-1. ECDSA Memory Blocks

| Memory             | Size (byte) | Starting Address* | Ending Address* | Access |
|--------------------|-------------|-------------------|-----------------|--------|
| ECDSA_MEM_M        | 64          | 0x280             | 0x2BF           | R/W    |
| ECDSA_MEM_R        | 32          | 0xA00             | 0xA1F           | R/W    |
| ECDSA_MEM_S        | 32          | 0xA20             | 0xA3F           | R/W    |
| ECDSA_MEM_Z        | 32          | 0xA40             | 0xA5F           | R/W    |
| ECDSA_MEM_Qx       | 32          | 0xA60             | 0xA7F           | R/W    |
| ECDSA_MEM_Qy       | 32          | 0xA80             | 0xA9F           | R/W    |

\* Address offset related to the ECDSA accelerator base address is provided in Table 4.3-2 in Chapter 4 System and Memory.