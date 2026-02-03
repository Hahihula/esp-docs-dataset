**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.9 EE.FFT.AMS.S16.LD.R32.DECP

**Subsection Titles and Content:**

- **Instruction Word:** 
  - 110110 sel[2:0] qz[1:2] qz[0:0] qy[2:0] qx[1:0] qx[0:0] qx[2:1] qx[1:0] qu[2:0] as[3:0] 111 qx[2]

- **Assembler Syntax:** 
  - EE.FFT.AMS.S16.LD.R32.DECP qu, as, qz, qx1, qx, qy, qx, sel2

- **Description**
  - It is a dedicated FFT instruction to perform addition, subtraction, multiplication, addition and subtraction, and shift operations on 16-bit data segments.
  - During the operation, the instruction forces the lower 4 bits of the access address in register as to O and loads the 16-byte data from the memory to register qu in the big-endian word order, namely, loads the segment [127:96] of the data to [31:0] of qu. After the access is completed, the value in register as is decreased by 16.

- **Operation**
  - (Code snippet with conditional operations based on the value of sel2)
    ```assembly
    if sel2==0:
        temp2[15:0] = ((qx[79:64] - qx[79:64]) * qm[79:64] - (qx[95:80] + qx[95:80])) >> SAR
    temp3[15:0] = ((qx[79:64] - qx[79:64]) * qm[95:80] + (qx[95:80] + qx[95:80])) >> SAR

    if sel2==1:
        temp2[15:0] = ((qx[95:80] + qx[95:80]) * qm[79:64] - (qx[79:64] + qx[79:64])) >> SAR
    temp3[15:0] = ((qx[95:80] + qx[95:80]) * qm[79:64] - (qx[79:64] - qx[79:64])) >> SAR

        qx[79:64] = temp0[15:0] + temp2[15:0]
        qx[95:80] = temp1[15:0] + temp3[15:0]
        qx[79:64] = temp0[15:0] - temp2[15:0]
        qx[95:80] = temp3[15:0] - temp1[15:0]

        {qu[31:0], qu[63:32], qu[95:64], qu[127:96]} = load128({as[31:4],4{0}})
        as[31:0] = as[31:0] - 16
    ```

**Footer Information:** 
- Espressif Systems, ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback