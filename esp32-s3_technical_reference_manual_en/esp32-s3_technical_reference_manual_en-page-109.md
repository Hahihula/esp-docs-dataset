**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.33 EE.LDQA.U16.I28.IP

**Subsection Titles and Content:**

- **Instruction Word:** 
  - `0 imm[7] 0001010 imm16[6:0] as[3:0] 0100`

- **Assembler Syntax**
  - Example syntax provided:
    ```
    EE.LDQA.U16.128.IP as, -2048..2032
    ```

- **Description**
  - This instruction forces the lower 4 bits of the access address in register `as` to zero, loads 16-byte data from memory, divides it into 8 segments of 16 bits, zero-extends each segment to 40 bits, and then stores the results to the 160-bit special registers QACC_L and QACC_H respectively. After the access is completed, the value in register `as` is incremented by an 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

- **Operation**
  - Detailed operation steps:
    ```
    dataIn[127:0] = load128({as[31:4],4{0}})
    
    QACC_L[ 39: 0] = {24{0}, dataIn[ 15: 0]}
    QACC_L[ 79: 40] = {24{0}, dataIn[ 31: 16]}
    QACC_L[119: 80] = {24{0}, dataIn[ 47: 32]}
    QACC_L[159:120] = {24{0}, dataIn[ 63: 48]}
    
    QACC_H[ 39: 0] = {24{0}, dataIn[ 79: 64]}
    QACC_H[ 79: 40] = {24{0}, dataIn[ 95: 80]}
    QACC_H[119: 80] = {24{0}, dataIn[111: 96]}
    
    QACC_H[159:120] = {24{0}, dataIn[127:112]}
    as[31:0] = as[31:0] + {20{imm16[7]}, imm16[7:0], 4{0}}
    ```

**Footer Information:** 
- "Espressif Systems"
- Page number and document version:
  - ESP32-S3 TRM (Version 1.7)
- Link to submit documentation feedback.

**Navigation Links:**
- GoBack

(Note: The text provided is a transcription of the visible content in the image, including any potential errors or inconsistencies.)