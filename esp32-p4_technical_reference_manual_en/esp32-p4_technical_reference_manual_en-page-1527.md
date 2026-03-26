

```markdown
- ECDSA_SHA_RELEASE_INT_CLR: set this bit to clear the ECDSA_SHA_RELEASE_INT interrupt status. By setting this bit to 1, fields ECDSA_SHA_RELEASE_INT_RAW and ECDSA_SHA_RELEASE_INT_ST will be cleared.

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.
```

## 31.6 Memory Blocks

ECDSA_DS's memory blocks store input data and output data of the operation.

Table 31.6-1. ECDSA_DS Memory Blocks

| Memory          | Size (byte) | Starting Address* | Ending Address* | Access |
|-----------------|-------------|-------------------|-----------------|--------|
| ECDSA_MEM_M     | 64          | 0x280             | 0x2BF           | R/W    |
| ECDSA_MEM_R     | 32          | 0xA00             | 0xA1F           | R/W    |
| ECDSA_MEM_S     | 32          | 0xA20             | 0xA3F           | R/W    |
| ECDSA_MEM_Z     | 32          | 0xA40             | 0xA5F           | R/W    |
| ECDSA_MEM_Qx    | 32          | 0xA60             | 0xA7F           | R/W    |
| ECDSA_MEM_Qy    | 32          | 0xA80             | 0xA9F           | R/W    |

\* Address offset related to the ECDSA_DS base address is provided in Table 7.3-2 in Chapter 7 System and Memory.
```