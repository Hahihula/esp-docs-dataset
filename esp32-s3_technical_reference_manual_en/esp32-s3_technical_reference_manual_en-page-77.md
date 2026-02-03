**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
18.2 EE.BITREV

**Subheading - Instruction Word:**
- 11 qa[2:1] 1101 qa[0] 1111011 as[3:0] O100

**Subheading - Assembler Syntax:**
EE.BITREV qa, as

**Subheading - Description:**
This instruction swaps the bit order of data of different bit widths according to the value of special register FFT_BIT_WIDTH. Then, it compares the data before and after the swap, takes the larger value, pads the higher bits with 0 until it has 16 bits, and writes the result into the corresponding data segment of register qa.

In the following, Switchx is a function that represents the bit inversion of the x-bit. Switch5(0b10100) = Ob00101. Here Ob10100 means 5-bit binary data.

**Subheading - Operation:**
- temp[15:0] = as[15:0]
- temp1[15:0] = as[15:0] + 1
- temp2[15:0] = as[15:0] + 2
- temp3[15:0] = as[15:0] + 3
- temp4[15:0] = as[15:0] + 4
- temp5[15:0] = as[15:0] + 5
- temp6[15:0] = as[15:0] + 6
- temp7[15:0] = as[15:0] + 7

**Subheading - Additional Code Snippet (continued):**
```plaintext
if FFT_BIT_WIDTH==3:
    Switch3(X[2:0]:=X[0:2]
        qa[ 15 : 0 ] := '13'h0, max(tmp[0:2],Switch3(tmp[0:2])))
    qa[ 31 : 16 ] := '13'h0, max(tmp1[2:0],Switch3(tmp1[2:0])))
    qa[ 47 : 32 ] := '13'h0, max(tmp2[2:0],Switch3(tmp2[2:0])))
    qa[ 63 : 48 ] := '13'h0, max(tmp3[2:0],Switch3(tmp3[2:0])))
    qa[ 79 : 64 ] := '13'h0, max(tmp4[2:0],Switch3(tmp4[2:0])))
    qa[ 95 : 80 ] := '13'h0, max(tmp5[2:0],Switch3(tmp5[2:0])))
    qa[127 : 96 ] := '13'h0

if FFT_BIT_WIDTH==4:
    Switch4(X[3:0]:=X[0:3]
        qa[ 15 : 0 ] := '12'h0, max(tmp[3:0],Switch4(tmp[3:0])))
        qa[ 31 : 16 ] := '12'h0, max(tmp1[3:0],Switch4(tmp1[3:0])))
        qa[ 47 : 32 ] := '12'h0, max(tmp2[3:0],Switch4(tmp2[3:0])))
        qa[ 63 : 48 ] := '12'h0, max(tmp3[3:0],Switch4(tmp3[3:0])))
        qa[ 79 : 64 ] := '12'h0, max(tmp4[3:0],Switch4(tmp4[3:0])))
        qa[ 95 : 80 ] := '12'h0, max(tmp5[3:0],Switch4(tmp5[3:0])))
        qa[111 : 96 ] := '12'h0, max(tmp6[3:0],Switch4(tmp6[3:0])))
        qa[127 : 112 ] := '12'h0, max(tmp7[3:0],Switch4(tmp7[3:0])))

if FFT_BIT_WIDTH==10:
    Switch10(X[9:0]:=X[0:9]
        qa[ 15 : 0 ] := '6'h0, max(tmp0[9:0],Switch10(tmp0[9:0])))
        qa[ 31 : 16 ] := '6'h0, max(tmp1[9:0],Switch10(tmp1[9:0])))
        qa[ 47 : 32 ] := '6'h0, max(tmp2[9:0],Switch10(tmp2[9:0])))
        qa[ 63 : 48 ] := '6'h0, max(tmp3[9:0],Switch10(tmp3[9:0])))
        qa[ 79 : 64 ] := '6'h0, max(tmp4[9:0],Switch10(tmp4[9:0])))
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback