**Chapter Title:**
Chapter 16 World Controller (WCL)

**Section Titles and Content:**

### 16.5.4 Nested Interrupts

ESP32-S3 supports nested interrupts, for example:

- An interrupt A occurs. CPU jumps to interrupt A entry, which triggers world switches.
- When CPU is handling interrupt A, an interrupt B with higher priority occurs.
- Then the CPU drops the current interrupt A and switches to the higher priority interrupt B first.
- After returning from interrupt B, CPU resumes executing the instruction at interrupt A entry, which triggers world switches again.

In this way, CPU executes the entry address of the first interrupt twice (one time when the interrupt occurs and another time when CPU returns to this interrupt), thus triggering the world switches twice, which inevitably leads to multiple records tracked for the same interrupt in World Switch Log and prevents the CPU from restoring to the previous world correctly.

### 16.5.4.1 How to Handle Nested Interrupts

To avoid multiple records being logged incorrectly in the World Switch Log, the following actions must be completed:

- During the design stage, add two assembly instruction NOP.N (No Operation) to the vector entrance of all interrupts and exceptions.
- During the execution, update the address where the interrupts return to following the instructions described in 16.5.4.2.

In this way, when returning to the interrupt at Entry B, the interrupt monitored at Entry A will not return to the entry address of Entry B, but the address after the NOP instructions, thus preventing to trigger the world controller unexpectedly. Also, the NOP instruction doesn’t do anything, so nothing is changed even when the NOP instructions are skipped.

### 16.5.4.2 Programming Procedure

Handling the interrupt at Entry A:

- Clear the write_buffer by writing the agreed sequences configured in Register WCL_CORE_m_MESSAGE_MAX_REG to the address configured in WCL_CORE_m_MESSAGE_ADDR_REG.
- For details, see Section 16.4.3.

- Execute the interrupt programs.

**Footer:**
Espressif Systems
809 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback