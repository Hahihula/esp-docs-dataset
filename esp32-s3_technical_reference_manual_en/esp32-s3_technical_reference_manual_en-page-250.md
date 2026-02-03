**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.168 EE.VMULAS.U16.QACC.LDBC.INCP

**Instruction Word Table:**
- qu[2]: O111
- q[1]: 0111
- qy[2]: 0100
- qu[0]: 
- qy[1:0]: 
- qx[2:0]: 
- as[3:0]: 

**Subheader - Assembler Syntax:**
EE.VMULAS.U16.QACC.LDBC.INCP qu, as, qx, qy

**Description Section:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then the unsigned multiplication result of the 8 sets of segments is added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 40-bit unsigned number and then stored to the corresponding 40-bit data segment in QACC_H and QACC_L.

At the same time, this instruction forces the lower 1 bit of the access address in register as to O, loads 16-bit data from memory, and broadcasts it to the eight 16-bit data segments in register qu. After the access, the value in register as is incremented by 2.

**Operation Section:**
```
QACC_L[39:0] = min(QACC_L[39:0] + qx[15:0], 2^{40}-1)
QACC_L[79:40] = min(QACC_L[79:40] + qx[31:16], 2^{40}-1)

...
QACC_L[159:120] = min(QACC_L[159:120] + qx[63:48], 2^{40}-1)
QACC_H[39:0] = min(QACC_H[39:0] + qx[79:64], 2^{40}-1)
QACC_H[79:40] = min(QACC_H[79:40] + qx[95:80], 2^{40}-1)

...
QACC_H[159:120] = min(QACC_H[159:120] + qx[127:112], 2^{40}-1)
qu[127:0] = {8{load16({as[31:1],1{0})}}
as[31:0] = as[31:0] + 2
```

**Footer Information:**
Espressif Systems  
Page Number: 250  
Document Title: ESP32-S3 TRM (Version 1.7)