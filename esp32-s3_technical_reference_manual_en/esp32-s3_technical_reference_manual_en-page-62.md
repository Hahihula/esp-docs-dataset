**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Table Header:**
Table 1.6-13. Shift Instructions

| Instructions | Description |
|--------------|-------------|
| EE.SRC.Q     | Perform logical right-shift on the spliced 16-byte data, and the shift value is determined by the SAR_BYTE register. |
| EE.SRC.Q.QUP  | Perform logical right-shift on the spliced 16-byte data, and the shift value is determined by the SAR_BYTE register. Meanwhile, the higher 8-byte data is saved. |
| EE.SRC.Q.LD.XP | Perform logical right-shift on the spliced 16-byte data, and the shift value is determined by the SAR_BYTE register. At the same time, read 16-byte data from memory and add a register value to the read address. |
| EE.SRC.Q.LD.IP | Perform logical right-shift on the spliced 16-byte data, and the shift value is determined by the SAR_BYTE register. At the same time, read 16-byte data from memory and add an immediate number to the read address. |
| EE.SLCI.2Q   | Perform logical left-shift on the spliced 16-byte data, and the shift value is determined by the immediate value. |
| EE.SLCXXP.2Q | Perform logical left-shift on the spliced 16-byte data, and the shift value is determined by the value in the AR register. |
| EE.SRCI.2Q   | Perform logical right-shift on the spliced 16-byte data, and the shift value is determined by the immediate value. |
| EE.SRCXXP.2Q | Perform logical right-shift on the spliced 16-byte data, and the shift value is determined by the value in the AR register. |
| EE.SRCQ.128.ST.INCP | Perform logical right-shift on the spliced 16-byte data, which will be written to memory after the shift. |
| EE.VSR.32   | Perform vector arithmetic right-shift on the 4-byte data. |
| EE.VSL.32   | Perform vector arithmetic left-shift on the 4-byte data. |

**Subsection Title:**
16.8 FFT Dedicated Instructions

**Body Text:**
FFT (Fast Fourier Transform) dedicated instructions include butterfly computation instructions, bit reverse instruction, and real number FFT instructions.

**Subsection Subtitle:**
Butterfly Computation Instructions

**Table Header for Butterfly Computation Instructions:**
Table 1.6-14. Butterfly Computation Instructions

| Instructions | Description |
|--------------|-------------|
| EE.FFT.R2BF.S16. | Perform radix-2 butterfly computation. |
| EE.FFT.R2BF.S16.ST.INCP | Perform radix-2 butterfly computation, and write the 16-byte result to memory at the same time. |
| EE.FFT.CMUL.S16.LD.XP | Perform radix-2 complex butterfly computation, and read 16-byte data from memory at the same time.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)