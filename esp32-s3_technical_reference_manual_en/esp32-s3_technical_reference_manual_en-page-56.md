**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Table Header:**
Table 1.6-4, Data Exchange Instructions

| Instructions | Description |
|--------------|-------------|
| MV.QR        | Move the value from the source QR register to the target QR register. |
| EE.MOV.I32.A | Assign a piece of 32-bit data from the QR register to the AR register. |
| EE.MOV.I32.Q | Assign the data stored in the AR register to a piece of 32-bit data space in the QR register. |
| EE.VZIP.[8/16/32] | Encoding the two QR registers in 1-byte/2-byte/4-byte unit. |
| EE.VUNZIP.[8/16/32] | Decoding the two QR registers in 1-byte/2-byte/4-byte unit. |
| EE.ZERO.Q    | Clear a specified QR register. |
| EE.ZERO.QACC | Clear QACC_H and QACC_L registers. |
| EE.ZERO.ACCX | Clear a specified ACCX register. |
| EE.MOV.S8.QACC | Slice the QR register by 1-byte, and sign-extend it to 20-bit data, then assign this value to QACC_H and QACC_L registers. |
| EE.MOV.S16.QACC | Slice the QR register by 2-byte, and sign-extend it to 40-bit data, then assign this value to QACC_H and QACC_L registers. |
| EE.MOV.U8.QACC | Slice the QR register by 1-byte, and zero-extend it to 20-bit, then assign this value to QACC_H and QACC_L registers. |
| EE.MOV.U16.QACC | Slice the QR register by 2-byte, and zero-extend it to 40-bit data, then assign this value to QACC_H and QACC_L registers. |

**Subsection Title:**
1.6.4 Arithmetic Instructions

**Body Text for Subsection:**
Arithmetic instructions mainly use the SIMD (Single Instruction Multiple Data) principle for vector data operations, including vector addition, vector multiplication, vector complex multiplication, vector multiplication accumulation, vector and scalar multiplication accumulation, etc.

Vector Addition Instructions
ESP32-S3 provides vector addition and subtraction instructions for data in 1-byte, 2-byte and 4-byte units.
Considering that the input and output operands required for vector operations are stored in memory, in order to reduce extra operations as reading memory and to improve the speed of code execution, vector addition instructions are designed to perform the addition and the 16-byte access at the same time, and the value in the address register is increased by 16 after the access, thus directly pointing to the next continuous 16-byte memory address. You can select the appropriate instruction according to the actual algorithm needs.
In addition, vector addition instructions also saturate the result of addition and subtraction to ensure the accuracy of arithmetic operations.

**Table Header:**
Table 1.6-5, Vector Addition Instructions

| Instructions | Description |
|--------------|-------------|
| EE.VADDS.S[8/16/32] | Perform vector addition operation on 1-byte/2-byte/4-byte data. |
| EE.VADDSP.S[8/16/32].LD.INC | Perform vector addition operation on 1-byte/2-byte/4-byte data, and read 16-byte data from memory at the same time.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback