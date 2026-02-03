**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**GoBack Link:** GoBack

**Table of Instructions and Operations**

| Instruction | Operation | Description |
|-------------|-----------|-------------|
| EE.VMIN.S16.LD.INCP | as 1, qx 1, qy 1 | qu 2, as 1, qa 1 |
| EE.VMIN.S16.ST.INCP | qv 1, as 1, qx 1, qy 1 | as 1, qa 1 |
| EE.VMIN.S32 | qx 1, qy 1 | qa 1 |
| EE.VMIN.S32.LD.INCP | as 1, qx 1, qy 1 | qu 2, as 1, qa 1 |
| EE.VMIN.S32.ST.INCP | qv 1, as 1, qx 1, qy 1 | as 1, qa 1 |
| EE.VMIN.S8 | qx 1, qy 1 | qa 1 |
| EE.VMIN.S8.LD.INCP | as 1, qx 1, qy 1 | qu 2, as 1, qa 1 |
| EE.VMIN.S8.ST.INCP | qv 1, as 1, qx 1, qy 1 | as 1, qa 1 |
| EE.VMUL.S16 | qx 1, qz 2 | SAR 1 |
| EE.VMUL.S16.LD.INCP | as 1, qx 1, qy 1 | qu 2, as 1, qx 2 |
| EE.VMUL.S16.ST.INCP | qx 1, qy 1 | as 1, qx 2 |
| EE.VMUL.S8 | qx 1, qy 1 | SAR 1 |
| EE.VMUL.S8.LD.INCP | as 1, qx 1, qy 1 | qu 2, as 1, qx 2 |
| EE.VMUL.S8.ST.INCP | qx 1, qy 1 | as 1, qx 2 |
| EE.VMUL.U16 | qx 1, qy 1 | SAR 1 |
| EE.VMUL.U16.LD.INCP | as 1, qx 1, qy 1 | qu 2, as 1, qx 2 |
| EE.VMUL.U16.ST.INCP | qx 1, qy 1 | as 1, qx 2 |
| EE.VMUL.U8 | qx 1, qy 1 | SAR 1 |
| EE.VMUL.U8.LD.INCP | as 1, qx 1, qy 1 | qu 2, as 1, qx 2 |
| EE.VMUL.U8.ST.INCP | qx 1, qy 1 | as 1, qx 2 |
| EE.VMULAS.S16.ACCX | qx 1, qy 1 | ACCX 2 |
| EE.VMULAS.S16.ACCX.LD.IP | as 1, qx 1, qy 1 | qu 2, as 1 |
| EE.VMULAS.S16.ACCX.LD.IP.QU | as 1, qx 1, qy 1, qs0 1, qs1 1 | SAR_BYTE 1, ACCX 2 |
| EE.VMULAS.S16.ACCX.LD.XP | as 1, ad 1, qx 1, qy 1 | qu 2, as 1 |
| EE.VMULAS.S16.ACCX.LD.XP.QU | as 1, ad 1, qx 1, qy 1, qs0 1, qs1 1 | SAR_BYTE 1, ACCX 2 |
| EE.VMULAS.S16.QACC | qx 1, qy 1 | QACC_H 2, QACC_L 2 |
| EE.VMULAS.S16.QACC.LD.IP | as 1, qx 1, qy 1 | qu 2, as 1 | QACC_H 2, QACC_L 2 |

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Page Number and Document Version:** ESP32-S3 TRM (Version 1.7)