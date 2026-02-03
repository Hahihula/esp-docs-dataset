**Title: Chapter 1 Processor Instruction Extensions (PIE)**

---

| Instruction | Operation | Register/Address | Offset | Access Mode |
|-------------|-----------|------------------|--------|-------------|
| EE.VMULAS.U16.ACCX.LD.XP.QU | as 1, ad 1, qx 1, qy 1 | qu 2, as 1, qs0 1 | SAR_BYTE | ACCX 2 |
| EE.VMULAS.U16.QACC | qx 1, qy 1 | — | QACC_L H 2 | QACC_L H 2 |
| EE.VMULAS.U16.QACC.LD.IP | as 1, qx 1, qy 1 | qu 2, as 1 | SAR_BYTE | QACC_H 2 |
| EE.VMULAS.U16.QACC.LD.IP.QU | as 1, qx 1, qy 1 | qu 2, as 1, qs0 1 | QACC_L H 2 | QACC_L L 2 |
| EE.VMULAS.U16.QACC.LD.XP | as 1, ad 1, qx 1, qy 1 | qu 2, as 1 | SAR_BYTE | QACC_H 2 |
| EE.VMULAS.U16.QACC.LD.IP.QU | as 1, ad 1, qx 1, qy 1 | qu 2, as 1, qs0 1 | QACC_L H 2 | QACC_L L 2 |
| EE.VMULAS.U8.ACCX | qx 1, qy 1 | — | ACCX 2 | ACCX 2 |
| EE.VMULAS.U8.ACCX.LD.IP | as 1, qx 1, qy 1 | qu 2, as 1 | SAR_BYTE | ACCX 2 |
| EE.VMULAS.U8.ACCX.LD.IP.QU | as 1, qx 1, qy 1 | qu 2, as 1, qs0 1 | QACC_L H 2 | QACC_L L 2 |
| EE.VMULAS.U8.ACCX.LD.XP | as 1, ad 1, qx 1, qy 1 | qu 2, as 1, qs0 1 | SAR_BYTE | ACCX 2 |
| EE.VMULAS.U8.QACC | qx 1, qy 1 | — | QACC_L H 2 | QACC_L L 2 |
| EE.VMULAS.U8.QACC.LD.IP | as 1, qx 1, qy 1 | qu 2, as 1 | SAR_BYTE | ACCX 2 |
| EE.VMULAS.U8.QACC.LD.IP.QU | as 1, qx 1, qy 1 | qu 2, as 1, qs0 1 | QACC_L H 2 | QACC_L L 2 |
| EE.VMULAS.U8.QACC.LD.XP | as 1, ad 1, qx 1, qy 1 | qu 2, as 1, qs0 1 | SAR_BYTE | ACCX 2 |
| EE.VMULAS.U8.QACC.LD.IP.QU | as 1, qx 1, qy 1 | qu 2, as 1, qs0 1 | QACC_L H 2 | QACC_L L 2 |

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)