**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Table of Contents Navigation:**
GoBack

**Section Header:**
wr_way write_cnt Store Data Operation

**Table Content Description with Headers and Values:**
- **0**: * Mem [Rdst + Offset]{31:0} = {PC[10:0], 3'b0, Label[1:0], Rsrc[15:0]} - Write full-word, including the pointer and the data
- **1 odd**: Mem [Rdst + Offset]{15:0} = {Label[1:0], Rsor[13:0]} - Store the data with label in the low half-word
- **1 even**: Mem [Rdst + Offset]{31:16} = {Label[1:0], Rscr[13:0]} - Store the data with label in the high half-word
- **3 odd**: Mem [Rdst + Offset]{15:0} = Rsor[15:0] - Store the data without label in the low half-word
- **3 even**: Mem [Rdst + Offset]{31:16} = Rsrc[15:0] - Store the data without label in the high half-word

**Table Caption and Description (Table 2.5-4):**
Data Storage Type - Automatic Storage Mode.

**Body Text Explanation of Table Content:**
The full-word written to RTC memory is built as follows:

**Figure Reference with Diagrams Descriptions:**
- **Figure 2.5-8**: Data Structure of RTC_SLOW_MEM[Rdst + Offset]
  - Bits Description:
    - bits [15:0]: store the content of Rsrc
    - bits [17:16]: data label, 2-bit user defined unsigned value
    - bits [20:18]: 3'b0 by default
    - bits [31:21]: hold the PC of current instruction, expressed in 32-bit words

**Note Section (Additional Information):**
- When full-word is written, the offset will be automatically incremented by 1 after each ST-AUTO-DATA execution.
- When half-word was written (low half-word first), the offset will be automatically incremented by 1 after twice ST-AUTO-DATA execution.
- This instruction can only access 32-bit memory words.

**Additional Information:**
The "Mem" written is the RTC_SLOW_MEM memory. Address O, as seen by the ULP coprocessor, corresponds to address Ox50000000, as seen by the main CPU.

**Section Header for Another Mode of Operation:**
Manual Storage Mode

**Figure Reference with Diagrams Descriptions (Continued):**
- **Figure 2.5-9**: Instruction Type - Data Storage in Manual Storage Mode
  - The diagram shows a bit map indicating different bits and their corresponding labels or values.

**Footer Information:**
Espressif Systems  
315  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback