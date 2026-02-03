**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Table Header:**
Table 1.4-1. Instruction Field Names and Descriptions

**Table Columns:**
Name | Description

**Table Entries:**

- **a***  
  - In-out type used as input/output operand.
  - Stores address information for read/write operations, which is updated after such operations are completed.

- **32-bit general-purpose registers at EE.FFT.AMS.S16.ST.NCP instruction**
  - Temporarily stores operation results to the data to be written to memory.  
  - In type (used as input operand). Stores data used to update address information.
  - Out type: Stores a result of an arithmetic or logical operation.

- **ax,ay**  
  - In type. Stores data involved in arithmetic operations such as shifting amounts and multipliers etc., e.g.,
  - Out type stores results from instruction operations (e.g., multiplication).

- **au**  
  - In type: Stores 128-bit data used for concatenation.

- **qs**  
  - In type. Stores vector operation result.
  - Out type, Stores the result of a vector operation or read from memory.

- **qz**  
  - Out type stores results of vector operations (e.g., multiplication).

- **qu**  
  - Out type: Stores data to be written in memory and used for concatenation with other registers like 'qs'.

- **qv**  
  - In type. Stores floating-point register.
  - 32-bit general-purpose floating-point register.

- **fu**  
  - Floating-point data read from memory (e.g., multiplication).

- **fv**  
  - 32-bit general-purpose floating-point register, stores floating-point data to be written in memory and used for concatenation with other registers like 'qs'.

- **sel2**  
  - 1-bit immediate value ranging from 0 to 1. Used to select signals.

- **sel4, upd4**  
  - 2-bit immediate value (0 or 3). Used to select signals.
  - 8-bit immediate value for selecting specific registers in the 'sel' field of an instruction operation code like 'sel8'.

- **sel8**  
  - 3-bit immediate value ranging from 0 to 7. Used to select signals.

- **sel16**  
  - 4-bit immediate value (0 or 15). Used for selecting specific registers in the 'sel' field of an instruction operation code like 'sel16'.

- **sar2, sar4, sar16**  
  - 1-bit to 4-bit values representing shifting numbers.

- **imm1**  
  - 7-bit unsigned immediate value (0 or up to 127) with intervals. Used for showing the size of updated read/write operation address value.
  - This is used in conjunction with 'sel' fields like 'sel8'.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)

**Note:** The text continues on to the next page, as indicated by "Cont'd on next page".