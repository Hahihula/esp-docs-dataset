**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header: Instructions**

- **Instruction:** EE.VADDS.S[8/16/32].ST.INC.P
  - **Description:** Perform vector addition operation on 1-byte/2-byte/4-byte data, and write 16-byte data to memory at the same time.

- **Instruction:** EE.VSUBS.S[8/16/32]
  - **Description:** Perform vector subtraction operation on 1-byte/2-byte/4-byte data.

- **Instruction:** EE.VSUBS.S[8/16/32].LD.INC.P
  - **Description:** Perform vector subtraction operation on 1-byte/2-byte/4-byte data, and read 16-byte data from memory at the same time.

- **Instruction:** EE.VSUBS.S[8/16/32].ST.INC.P
  - **Description:** Perform vector subtraction operation on 1-byte/2-byte/4-byte data, and write 16-byte data to memory at the same time.

**Section Header: Vector Multiplication Instructions**

- ESP32-S3 provides vector multiplication instructions for data in 1-byte and 2-byte units, and supports unsigned and signed vector multiplication.
  
- **Instruction Table (Table 1.6-6):**
  - **Instructions:** EE.VMUL.U[8/16]
    - Perform vector multiplication operation on unsigned 1-byte/2-byte data.

  - **Instructions:** EE.VMUL.S[8/16]
    - Perform vector multiplication operation on signed 1-byte/2-byte data.
  
  - **Instructions:** EE.VMUL.U[8/16].LD.INC.P
    - Perform vector multiplication operation on unsigned 1-byte/2-byte data, and read 16-byte data from memory at the same time.

  - **Instructions:** EE.VMUL.S[8/16].LD.INC.P
    - Perform vector multiplication operation on signed 1-byte/2-byte data, and read 16-byte data from memory at the same time.
  
  - **Instructions:** EE.VMUL.U[8/16].ST.INC.P
    - Perform vector multiplication operation on unsigned 1-byte/2-byte data, and write 16-byte data to memory at the same time.

  - **Instructions:** EE.VMUL.S[8/16].ST.INC.P
    - Perform vector multiplication operation on signed 1-byte/2-byte data, and write 16-byte data to memory at the same time.
  
- Considering that the input and output operands required for vector operations are stored in memory, in order to reduce extra operations as reading memory and improve the speed of code execution, vector multiplication instructions are designed to perform the multiplication and access 16 bytes at the same time. The access address is increased by 16 after the access; thus directly pointing to the next 16-byte memory address.

**Section Header: Vector Complex Multiplication Instructions**

- ESP32-S3 provides vector complex multiplication instructions for data in 2-byte unit.
  
- **Instruction Description:** 
  - Considering that the input and output operands required for vector operations are stored in memory, in order to reduce extra operations as reading memory and improve the speed of code execution, vector complex multiplication instructions are designed to perform the multiplication and access 16 bytes at the same time. The access address is increased by 16 after the access; thus directly pointing to the next 16-byte memory address.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback