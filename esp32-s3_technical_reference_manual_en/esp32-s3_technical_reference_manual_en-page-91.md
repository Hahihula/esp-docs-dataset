**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.15 EE.FFT.VST.R32.DECP

**Instruction Word Table:**
- 11 | qv[2:1] | 1101 | qv[0] | 0110 | sar2[0] | 11 | as[3:0] | 0100

**Subheading - Assembler Syntax:**
EE.FFT.VST.R32.DECP qv, as, sar2

**Description Section:**
It is a dedicated FFT instruction. This instruction divides data in register qv into 8 segments of 16-bit data and performs an arithmetic right shift on them by 0 or 1 depending on the immediate number sar2, and finally writes the result to the memory address indicated by register as in word big-endian order. After the access is completed, the value in register as is decreased by 16.

**Operation Section:**
```
{
    qv[ 31: 16 ] >> sar2,
    qv[ 15: 0 ] >> sar2,
    qv[ 63: 48 ] >> sar2,
    qv[ 47: 32 ] >> sar2,
    qv[ 95: 80 ] >> sar2,
    qv[ 79: 64 ] >> sar2,
    qv[127:112] >> sar2,
    qv[111: 96 ] >> sar2
}
=> store128({as[31:4],4{0}})
as[31:0] = as[31:0] - 16
```