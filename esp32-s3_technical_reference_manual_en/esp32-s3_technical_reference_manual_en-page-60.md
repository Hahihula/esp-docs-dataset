**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading: Vector and Scalar Multiplication Accumulation Instructions**

**Body Text:**
The function of this type of instructions is similar to that of the vector multiplication accumulation instructions based on QACC_H and QACC_L registers, except that one of the binocular operands is a vector and the other is a scalar. It also contains instructions that can execute access operation while vector operations are performed.

**Table 1.6-9: Vector and Scalar Multiplication Accumulation Instructions**

| Instructions | Description |
|--------------|-------------|
| EE.VSMULAS.S[8/16].QACC | Perform vector and scalar multiplication accumulation on signed data in 1-byte/2-byte segment. |
| EE.VSMULAS.S[8/16].QACC.LD.INCP | Perform vector and scalar multiplication accumulation on signed data in 1-byte/2-byte segment, and read 16-byte data from memory at the same time. Add 16 to address register. |

**Subsection Heading: Other Instructions**

**Body Text:**
This section contains instructions that perform arithmetic right-shifting on multiplication accumulation results in QACC_H, QACC_L and ACCX. You can set the shifting value to obtain the multiplication accumulation results within the expected accuracy range.

In addition, it also contains vector multiplication instructions with enabling conditions.

**Table 1.6-10: Other Instructions**

| Instructions | Description |
|--------------|-------------|
| EE.SRCMB.S[8/16].QACC | Perform signed right-shifting on data in QACC_H and QACC_L registers in segment unit. |
| EE.SRS.ACCX | Perform signed right-shifting on data in the ACCX register. |
| EE.VRELU.S[8/16] | Perform vector and scalar multiplication based on enabling conditions. |
| EE.VPRELU.S[8/16] | Perform vector-to-vector multiplication based on enabling conditions. |

**Subsection Heading: 1.6.5 Comparison Instructions**

**Body Text:**
Vector comparison instructions compare data in the unit of 1 byte, 2 bytes, or 4 bytes, including the instructions that take the larger/smaller one between the compared two values, that set all bits to 1 when the two values are equal and set them to 0 when they are not equal, that set all bits to 1 when the former value is larger than the latter and otherwise set them to 0, and that set all bits to 1 when the former value is smaller than the latter and otherwise set them to 0.

Considering that the input and output operands required for vector operations are stored in memory, in order to reduce extra operations as reading memory and improve the speed of code execution, access instructions to 16-byte addresses are performed at the same time as vector operations, and the access address is increased by 16 after the access, thus directly pointing to the next 16-byte memory address. You can select the appropriate instruction according to the actual algorithm needs.

**Footer:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)