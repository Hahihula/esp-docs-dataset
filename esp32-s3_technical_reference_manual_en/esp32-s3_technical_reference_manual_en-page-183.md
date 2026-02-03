**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.107 EE.VMAX.S32

**Subsection - Instruction Word:**
- 10 qa[2:1] 1110 qa[0] qx[2] 1 qx[1:0] qx[2:0] 00110100

**Subsection - Assembler Syntax:**
EE.VMAX.S32 qa, qx, qy

**Subsection - Description:**
This instruction compares numerical values of the four 32-bit vector data segments in registers qx and qy. The data segment with the larger value is written into the corresponding 32-bit data segment in register qa.

**Subsection - Operation (with code example):**
```
1    qa[ 31: 0 ] = (qx[ 31: 0 ] >=qy[ 31: 0 ]) ? qx[ 31: 0 ] : qy[ 31: 0 ]
2    qa[ 63: 32 ] = (qx[ 63: 32 ] >=qy[ 63: 32 ]) ? qx[ 63: 32 ] : qy[ 63: 32 ]
3
4    qa[127: 96 ] = (qx[127: 96] >=qy[127: 96]) ? qx[127: 96] : qy[127: 96]
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback