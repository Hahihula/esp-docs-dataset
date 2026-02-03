**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.104 EE.VMAX.S16

**Instruction Word Syntax:**
```
10 qa[2:1] 1110 qa[0] qy[2] 1 qy[1:0] qx[2:0] 00100100
```

**Assembler Syntax Title:**
Assembler Syntax

**Description Section:**
- **Title:** Description
- **Content:** This instruction compares numerical values of the eight 16-bit vector data segments in registers qx and qy. The data segment with the larger value is written into the corresponding 16-bit data segment in register qa.

**Operation Title:**
Operation

**Operation Details (List):**
```
qa[ 15 : 0 ] = (qx[ 15 : 0 ]>=qy[ 15 : 0 ]) ? qx[ 15 : 0 ] : qy[ 15 : 0 ]
qa[31 : 16] = (qx[31:16]>qy[31:16])? qx[31:16]: qy[31:16]
...
qa[127:112] = (qx[127:112]>=qy[127:112]) ? qx[127:112] : qy[127:112]
```

**Footer Information:**
- **Company:** Espressif Systems
- **Document Version and Type:** ESP32-S3 TRM (Version 1.7)
- **Link Texts:** Submit Documentation Feedback

**Navigation Link:**
GoBack