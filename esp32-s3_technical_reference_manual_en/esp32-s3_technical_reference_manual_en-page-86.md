**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
18.10 EE.FFT.AMS.S16.ST.INCP

**Instruction Word Table:**
- sel2[0]
- qz1[2:1]
- qmn[0]
- qv[2:0]
- qx1[0]
- qx[2:0]
- qy[1:0]
- qm[2:1]
- as[3:0]
- at[3:0]

**Assembler Syntax Table:**
- 10100
- 111

**Description Section:**
It is a dedicated FFT instruction to perform addition, subtraction, multiplication, addition and subtraction, and shift operations on 16-bit data segments.

During the operation, the instruction forces the lower 4 bits of the access address in register as to 0, splices the values in registers qv and at into 16-byte data, and stores the spliced result to memory. After the access is completed, the value in register as is incremented by 16. Besides, the operation result is updated to register at.

**Operation Section:**
```plaintext
temp0[15:0] = qx[111:96] + qy[111:96]
temp1[15:0] = qx[127:112] - qy[127:112]

if sel2==0:
    temp2[15:0] = ((qx[11:96] - qx[11:96]) * qx[11:96]) + qx[127:112]
                   + (qx[127:112]) * qm[127:112]) >> SAR[5:0]
temp3[15:0] = ((qx[11:96] - qx[11:96]) * qx[11:96]) + qx[127:112]
                   + (qx[127:112]) * qm[127:112]) >> SAR[5:0]

    [qv[ 95:80 ] > 1, qv[ 79:64 ] >> 1, qx[ 63:48 ] > 1, qx[ 47:32 ] >> 1, qx[ 31:
                   16 ]] > 1, qx[ 15:0 ] >> 1, at[31:16] >> 1, at[15:0]] >> 1 => store128({as
                   [31:4],4{0}})

if sel2==1:
    temp2[15:0] = ((qx[127:112] + qx[127:112]) * qx[127:112])
                   + (qx[111:96]) - qy[111:96])
temp3[15:0] = ((qx[127:112] + qx[127:112]) * qx[111:96])
                   - (qx[111:96]) - qy[111:96])

    qx[ 95:64 ], qx[ 63:32 ], qx[ 31:0 ], at[31:0]] => store128({as[31:4],4{0}})

temp4[16:0] = temp1[15:0] + temp3[15:0]
temp5[16:0] = temp0[15:0] + temp2[15:0]

qz1[111:96] = temp0[15:0] - temp1[15:0]
qz1[127:112] = temp3[15:0] - temp1[15:0]

at = {temp4[15:0], temp5[15:0]}
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems, ESP32-S3 TRM (Version 1.7), Page number is not explicitly mentioned but can be inferred from the context.

**Navigation Links:**
- GoBack

**Action Links:**
- Submit Documentation Feedback