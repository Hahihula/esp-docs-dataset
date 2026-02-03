**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.211 EE.VZIP.32

**Instruction Word:**
- 11 qs[2:1] 1100 qs[0] qsO[2:0] O01111000100

**Assembler Syntax:**
EE.VZIP.32 qsO, qs1

**Description:**
This instruction implements the zip algorithm on 32-bit vector data.

**Operation (List):**
```
qsO[ 31 : 0 ] = qsO[ 31 : 0 ]
qsO[ 63 : 32 ] = qs1[ 31 : 0 ]
qsO[ 95 : 64 ] = qsO[ 63 : 32 ]
qsO[127 : 96 ] = qs1[ 63 : 32 ]

qsI[ 31 : 0 ] = qsO[ 95: 64 ]
qsI[ 63 : 32 ] = qsI[ 95: 64 ]
qsI[ 95 : 64 ] = qsO[127: 96 ]
qsI[127 : 96 ] = qsI[127: 96 ]
```

**Footer Information:**
- Espressif Systems
- Page number: 294
- Document version and title: ESP32-S3 TRM (Version 1.7)
- Link: Submit Documentation Feedback