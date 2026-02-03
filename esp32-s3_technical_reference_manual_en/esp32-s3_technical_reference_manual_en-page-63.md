**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
Bit Reverse Instruction

**Body Text:**
The reverse bit width of this instruction is determined by the value in the FFT_BIT_WIDTH register.

**Table Caption and Table Content:**
- **Table 1.6-15. Bit Reverse Instruction**

| Instruction | Description |
|-------------|-------------|
| EE.BITREV   | Bit reverse instruction. |

**Section Header:**
Real Number FFT Instructions

**Body Text:**
A single real number FFT instruction can perform a series of complex calculations including addition, multiplication, shifting, etc.

**Table Caption and Table Content:**
- **Table 1.6-16. Real Number FFT Instructions**

| Instruction | Description |
|-------------|-------------|
| EE.FFT.AMS.S16.LD.INCPUAUP | Perform complex calculations and read 16-byte data from memory at the same time, then output 16-byte aligned data. |
| EE.FFT.AMS.S16.LD.INCP   | Perform complex calculations and read 16-byte data from memory at the same time. Add 16 to address register. |
| EE.FFT.AMS.S16.LD.R32.DECP | Perform complex calculations and read 16-byte data from memory at the same time. Reverse the word order of read data. Add 16 to address register. |
| EE.FFT.AMS.S16.ST.INCP   | Perform complex calculation and write 16-byte data (consists of the data in AR and partial data segments in QR) to memory at the same time. |
| EE.FFT.VST.R32.DECP   | Splice the QR register in 2-byte unit, shift the result and write this 16-byte data to memory. |

**Section Header:**
1.6.9 GPIO Control Instructions

**Body Text:**
GPIO control instructions include instructions to drive GPIO_OUT and get the status of GPIO_IN.

**Table Caption and Table Content:**
- **Table 1.6-17. GPIO Control Instructions**

| Instruction | Description |
|-------------|-------------|
| EE.WR_MASK_GPIO_OUT   | Set GPIO_OUT by mask. |
| EE.SET_BIT_GPIO_OUT   | Set GPIO_OUT. |
| EE.CLR_BIT_GPIO_OUT   | Clear GPIO_OUT. |
| EE.GET_GPIO_IN        | Get the status of GPIO_IN. |

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback