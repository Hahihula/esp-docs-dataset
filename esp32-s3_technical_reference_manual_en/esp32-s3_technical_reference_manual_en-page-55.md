**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Body Text:**
access addresses, except for the EE.STXQ.32 instruction, which selects a piece of 16-bit data first from the QR register via an immediate value, adds it to the access address, and then issues the access operation.

Since access to non-aligned addresses will cause slower response; all virtual addresses issued by write instructions in the extended instruction set are forced to be aligned according to data format. Depending on the size of the access data format, corresponding length of data will be written to memory as 1-byte, 2-byte, 4-byte, 8-byte or 16-byte. When the data length to be written to memory is less than the access bit length, it is necessary to perform zero extension or sign extension on this data.

The table below briefly describes the access operations performed by write instructions. For detailed information, please refer to Section 1.8.

**Table Title:**
Table 1.6-3. Write Instructions

| Instructions | Description |
|--------------|-------------|
| ST.QR        | Store 16-byte from QR to memory. |
| EE.VST.128.XP | Write the 16-byte data to memory, then add the value stored in the AR register to the access address. |
| EE.VST.128.IP | Write the 16-byte data to memory, then add the immediate value to the access address. |
| EE.VST.[H/L].64.XP | Write the 8-byte data to memory, then add the value stored in the AR register to the access address. |
| EE.VST.[H/L].64.IP | Write the 8-byte data to memory, then add the immediate value to the access address. |
| EE.STF.[64/128].XP | Write the 8-byte/16-byte data to memory, then add the value stored in the AR register to the access address. |
| EE.STF.[64/128].IP | Write the 8-byte/16-byte data to memory, then add the immediate value to the access address. |
| EE.ST.QACC_[H/L].32.IP | Write the 4-byte data to memory, then add the immediate value to the access address. |
| EE.ST.QACC_[H/L].128.IP | Write the 16-byte data to memory, then add the immediate value to the access address. |
| EE.ST.ACCX.IP | Zero-extend the value in the ACCX register to 8-byte data and write it to memory, then add the immediate value to the access address. |
| EE.ST.UA_STATE.IP | Write the 16-byte data to memory, then add the immediate value to the access address. |
| EE.STXQ.32   | Update the access address first, then write the 4-byte data to memory. |

**Subsection Title:**
1.6.3 Data Exchange Instructions

**Subsection Body Text:**
Data exchange instructions are mainly used to exchange data information between different registers. Considering the bit width of the exchange registers are different, the immediate value are added as the selection signal, and zero extension and sign extension instructions are provided also. A variety of data exchange instructions can meet the data exchange requirements for users under various scenarios.

For detailed information about data exchange instructions, please refer to Section 1.8.

**Footer:**
Espressif Systems  
55  
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)