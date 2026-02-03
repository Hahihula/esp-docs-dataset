**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.117 EE.VMIN.S32.LD.INCP

**Instruction Word Table:**
- qu[2:1] | qy[0] | O11 | qu[0] | qa[2:0] | qx[1:0] | qy[2:1] | 1110 | as[3:0] | 111 | qx[2]
- Value examples (hexadecimal): "111000" for qu[2:1], "O11" for qy[0], etc.

**Assembler Syntax Heading:**
Assembler Syntax

**Syntax Example:**
EE.VMIN.S32.LD.INCP qu, as, qa, qx, qy

**Description Section:**
This instruction compares numerical values of the four 32-bit vector data segments in registers qx and qy. The data segment with the smaller value is written into the corresponding 32-bit data segment in register qa.

During the operation:
- The lower 4 bits of the access address in register as are forced to be 0.
- Then, a 16-byte data is loaded from the memory to register qu.
- After this process, the value in register as (access address) is incremented by 16 bytes.

**Operation Section:**
```plaintext
qa[31: 0] = θ : (qx[31: 31] <= qy[31: 0]) ? qx[31: 0] : qy[31: 0]
qa[63: 32] = (qx[63: 32] <= qy[63: 32]) ? qx[63: 32] : qy[63: 32]

...
qa[127: 96] = (qx[127: 96] <= qy[127: 96]) ? qx[127: 96] : qy[127: 96]

qu[127:0] = load128({as[31:4],4{θ}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems  
Page number and document version information at the bottom.