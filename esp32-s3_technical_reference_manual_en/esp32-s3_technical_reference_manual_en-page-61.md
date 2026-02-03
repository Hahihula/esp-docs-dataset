**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Table of Contents:**

- **Section 16.5 Comparison Instructions**
  - Table 1.6-11, Comparison Instructions

| Instructions | Description |
|--------------|-------------|
| EE.VMAX.S[8/16/32] | Take the larger value between the two 1-byte/2-byte/4-byte values. |
| EE.VMAX.S[8/16/32].LD.INCP | Take the larger value between the two 1-byte/2-byte/4-byte values, and read 16-byte data from memory at the same time. |
| EE.VMAX.S[8/16/32].ST.INCP | Take the larger value between the two 1-byte/2-byte/4-byte values, and write 16-byte data to memory at the same time. |
| EE.VMIN.S[8/16/32] | Take the smaller value between the two 1-byte/2-byte/4-byte values. |
| EE.VMIN.S[8/16/32].LD.INCP | Take the smaller value between the two 1-byte/2-byte/4-byte values, and read 16-byte data from memory at the same time. |
| EE.VMIN.S[8/16/32].ST.INCP | Take the smaller value between the two 1-byte/2-byte/4-byte values, and write 16-byte data to memory at the same time. |
| EE.VCMP.EQ.S[8/16/32] | Compare two 1-byte/2-byte/4-byte values, set all bits to 1 when the two values are equal, or set all bits to 0 when they are not equal. |
| EE.VCMP.LT.S[8/16/32] | Compare two 1-byte/2-byte/4-byte values, set all bits to 1 when the former value is smaller than the latter one, or set them to 0 otherwise. |
| EE.VCMP.GT.S[8/16/32] | Compare two 1-byte/2-byte/4-byte values, set all bits to 1 when the former value is larger than the latter one, or set them to 0 otherwise.

- **Section 16.6 Bitwise Logical Instructions**
  - Table 1.6-12, Bitwise Logical Instructions

| Instructions | Description |
|--------------|-------------|
| EE.ORQ | Bitwise logical OR q = qx ∣∣ yy |
| EE.XORQ | Bitwise logical XOR qa = qx ∧ yyyy |
| EE.ANDQ | Bitwise logical AND qa = qx & yyyq |
| EE.NOTQ | Bitwise NOT qa = ~qx |

- **Section 16.7 Shift Instructions**
  - Description: 
    "Shift instructions include vector left-shift and vector right-shift instructions in 4-byte processing units as well as left-shift and right-shift instructions for spliced 16-byte data. The shift value of the former type is determined by the SAR_BYTE register; while the shift value of the latter type can be determined by the SAR, the immediate value, or the lower bits in the AR register. You can select appropriate instructions based on your application needs.
    All the shift instructions mentioned above are performed based on signed bits."

**Footer:**
Espressif Systems
61 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback