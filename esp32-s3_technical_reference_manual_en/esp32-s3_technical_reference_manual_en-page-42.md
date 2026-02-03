**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.4 Syntax Description

**Body Text:**
This section provides introduction to the encoding order of instructions and the meaning of characters that appear in the instruction descriptions.

**Subsection Header:**
1.4.1 Bit/Byte Order

**Subsection Body Text:**
The encoding order of instructions is divided into two types based on the granularity, i.e., bit order and byte order. According to the located side of the least bit or byte, there are big-endian order and little-endian order. That is to say, the most common encoding types for instructions are: little-endian bit order, big-endian bit order, little-endian byte order and big-endian byte order.

- Little-endian bit order: the instruction is encoded in bit order, with the least significant bit on the right.
- Big-endian bit order: the instruction is encoded in bit order, with the least significant bit on the left.
- Little-endian byte order: the instruction is encoded in byte order, with the least significant byte on the right.
- Big-endian byte order: the instruction is encoded in byte order, with the least significant byte on the left.

Among them, the instruction encoding bit sequences obtained using little-endian byte order and little-endian bit order are identical. Taking the 24-bit instruction EE.ZERO.QACC as an example, Figure 1.4-1, Figure 1.4-2, Figure 1.4-3 and Figure 1.4-4 show the code of this instruction in little-endian bit order, big-endian bit order, little-endian byte order and big-endian byte order, respectively.

Please note that all instructions and register descriptions appear in this chapter use little-endian bit order, which means the least significant bit is stored in the lowest addresses.

**Figure Captions:**
- Figure 1.4-1 shows "EE.ZERO.QACC in Little-Endian Bit Order"
- Figure 1.4-2 shows "EE.ZERO.QACC in Big-Endian Bit Order"

**Diagram Descriptions (partially represented as text):**
- The diagram for little-endian bit order is a sequence of bits labeled from most-significant to least-significant, with the instruction code displayed below.
- The diagram for big-endian bit order shows an identical arrangement but starting at 0 and moving towards higher numbers.

**Footer:**
Espressif Systems
42 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback