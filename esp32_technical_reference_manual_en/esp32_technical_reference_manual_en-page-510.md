**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register PMT_RWUFR_REG (0x1028)

**Diagram Description and Legend:**
- Diagram of a register with bits labeled from bit 3 to bit 0.
- Bits are numbered as follows:
  - Bit [31:0] is the byte mask. 
  - If Bit 1/2/3/4 (byte number) of the byte mask is set, the CRC block processes the filter 0/1/2/3 Offset + j of the incoming packet.
- The register bits are labeled as:
  - RWKPTR is O: Filter 0 Byte Mask;
  - RWKPTR is I: Filter 1 Byte Mask;
  - RWKPTR is II: Filter 2 Byte Mask;
  - RWKPTR is III: Filter 3 Byte Mask;

**Text Description of Register Bits and Their Functions:**
- **RWKPTR is O:** This bit defines the destination address type, specifying whether it's for multicast or unicast packets.
- **RWKPTR is I:** This filter examines offset bits [15:0] from a specific register (bit[31:16]).
- **RWKPTR is II:** This filter uses polynomial calculations to determine CRC values and byte masks based on the pattern.

**Polynomial Details for RWKPTR is O, I, and II:**
- For RWKPTR = 0:
  - Polynomial G(x) = x^16 + x^5 + x^2 + 1.
  
- For RWKPTR = I (Filter 1 Byte Mask):
  - Polynomial details are not provided in the text.

- For RWKPTR = II (Filter 2 Byte Mask):
  - Polynomial:
    G(x) = x^16 + x^5 + x^3 + 1. 

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32 TRM (Version 5.6)

**Navigation Link:**
GoBack