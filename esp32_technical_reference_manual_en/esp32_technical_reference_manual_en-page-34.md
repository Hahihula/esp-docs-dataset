**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Section Header:**
Operand Description

**Subsection Content with Code Block and Descriptions:**

- **Offset:** 
  - Description: 10-bit signed value, offset expressed in 32-bit words
  
- **Rsrc:**
  - Description: Register R[0-3], 16-bit value to store
  
- **Rdst:**
  - Description: Register R[0-3], address of the destination, expressed in 32-bit words

**Description Section:**

The instruction stores the 16-bit value of `Rsrc` in the lower half-word of memory with address `Rdst + Offset`. The upper half-word is written with the current program counter (PC) (expressed in words and shifted to the left by 5 bits) OR’d with `Rdst`.

**Note:**
- This instruction can only access 32-bit memory words.
- Data from `Rsrc` is always stored in the lower 16 bits of a memory word. Differently put, it is not possible to store `Rsrc` in the upper 16 bits of memory.

The "Mem" written is the RTC_SLOW_MEM memory. Address O, as seen by the ULP coprocessor, corresponds to address Ox50000000, as seen by the main CPUs.

**Figure Caption:**
- Figure 1.4-6. Instruction Type — LD

**Subsection Header with Diagram and Description:**

1.4.3 LD – Load Data from Memory

**Diagram (LD Instruction):**
- Offset
- Rsrc
- Rdst
  
**Operand Description - see Figure 1.4-6:**

- **Offset:** 
  - Description: 10-bit signed value, offset expressed in 32-bit words
  
- **Rsrc:**
  - Description: Register R[0-3], address of destination memory, expressed in 32-bit words
  
- **Rdst:**
  - Description: Register R[0-3], destination

**Description Section for LD Instruction:**

The instruction loads the lower 16-bit half-word from memory with address `Rsrc + Offset` into the destination register `Rdst`.

**Note:**
- This instruction can only access 32-bit memory words.
- In any case, it is always the lower 16 bits of a memory word that are loaded. Differently put, it is not possible to read the upper 16 bits.

The "Mem" loaded is the RTC_SLOW_MEM memory. Address O, as seen by the ULP coprocessor, corresponds to address Ox50000000, as seen by the main CPUs.

**Footer:**
- Espressif Systems
- Submit Documentation Feedback

**Document Version Information:** 
- ESP32 TRM (Version 5.6)