**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.108 EE.VMAX.S32.LD.INCP

**Instruction Word Table:**
- qu[2:1]: 001
- qu[0]: 001
- qa[2:0]: 001
- qx[1:0]: 001
- qy[2:1]: 1110 as[3:0]
- qx[2]

**Assembler Syntax Table:**
- EE.VMAX.S32.LD.INCP qu, as, qx, qy

**Description Section:**
This instruction compares numerical values of the four 32-bit vector data segments in registers qx and qy. The data segment with the larger value is written into the corresponding 32-bit data segment in register qa.

During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access, the value in register as is incremented by 16.

**Operation Section:**
- `qa[31: 0] = (qx[31: 0]>qy[31: 0]) ? qx[31: 0] : qy[31: 0]`
- `qa[63: 32] = (qx[63: 32]>qy[63: 32]) ? qx[63: 32] : qy[63: 32]`

**Additional Operations Listed:**
```
qa[127: 96] = (qx[127: 96]>qy[127: 96]) ? qx[127: 96] : qy[127: 96]
qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
- Page number: 184
- Document version and title: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems

**Navigation Links:**
- GoBack button at the top right corner.
- Submit Documentation Feedback link at the bottom center.

(Note: The text in the image is structured as described above, including tables and code blocks.)