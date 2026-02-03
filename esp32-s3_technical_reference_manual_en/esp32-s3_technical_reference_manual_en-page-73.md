**Title: Chapter 1 Processor Instruction Extensions (PIE)**

---

| Instruction | Description | QACC_H | QACC_L |
|-------------|-------------|--------|--------|
| EE.VMULAS.U8.QACC.LDBC.INCP.QUP | as 1, qx 1, qy 1<br>qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, QACC_L 2 |
| EE.VPRELU.S16 | qx 1, qy 1, ay 1 | qz 2 | — |
| EE.VPRELU.S8 | qx 1, qy 1, ay 1 | qz 2 | — |
| EE.VRELU.S16 | qs 1, ax 1, ay 1 | qs 2 | — |
| EE.VRELU.S8 | qs 1, ax 1, ay 1 | qs 2 | — |
| EE.VSL.32 | qs 1 | qa 1 | SAR 1 |
| EE.VSMULAS.S16.QACC | qx 1, qy 1 | — | QACC_H 2, QACC_L 2 |
| EE.VSMULAS.S16.QACC.LD.INCP | as 1, qx 1, qy 1 | qu 2, as 1 | QACC_H 2, QACC_L 2 |
| EE.VSMULAS.S8.QACC | qx 1, qy 1 | — | QACC_L 2, QACC_H 2 |
| EE.VSMULAS.S8.QACC.LD.INCP | as 1, qx 1, qy 1 | qu 2, as 1 | QACC_H 2, QACC_L 2 |
| EE.VSR.32 | qs 1 | qa 1 | SAR 1 |
| EE.VST.128.IP | qv 1, as 1 | as 1 | — |
| EE.VST.128.XP | qv 1, as 1, ad 1 | as 1 | — |
| EE.VST.H.64.IP | qv 1, as 1 | as 1 | — |
| EE.VST.L.64.IP | qv 1, as 1 | as 1 | — |
| EE.VSUBS.S16 | qx 1, qy 1 | qa 1 | — |
| EE.VSUBS.S16.LD.INCP | qs 1, ax 1, qx 1 | qu 2, as 1, qa 1 | — |
| EE.VSUBS.S16.ST.INCP | qx 1, as 1, qx 1, qy 1 | as 1, qa 1 | — |
| EE.VSUBS.S32 | qx 1, qy 1 | qa 1 | — |
| EE.VSUBS.S32.LD.INCP | qs 1, ax 1, qx 1, qy 1 | qu 2, as 1, qa 1 | — |
| EE.VSUBS.S8 | qx 1, qy 1 | qa 1 | — |
| EE.VSUBS.S8.LD.INCP | qs 1, ax 1, qx 1, qy 1 | qu 2, as 1, qa 1 | — |
| EE.VSUBS.S8.ST.INCP | qs 1, ax 1, qx 1, qy 1 | as 1, qa 1 | — |
| EE.VUNZIP.16 | qs0 1, qs1 1 | qs0 1, qs1 1 | — |
| EE.VUNZIP.32 | qs0 1, qs1 1 | qs0 1, qs1 1 | — |
| EE.VUNZIP.8 | qs0 1, qs1 1 | qs0 1, qs1 1 | — |
| EE.VZIP.16 | qs0 1, qs1 1 | qs0 1, qs1 1 | — |
| EE.VZIP.32 | qs0 1, qs1 1 | qs0 1, qs1 1 | — |
| EE.VZIP.8 | qs0 1, qs1 1 | qs0 1, qs1 1 | — |
| EE.WR_MASK_GPIO_OUT | as 1, ax 1 | — | GPIO_OUT 1 |
| EE.XORQ | qx 1, qy 1 | qa 1 | — |
| EE.ZERO.ACCX | — | — | ACCX 1 |

---

*Espressif Systems*

73

**Submit Documentation Feedback**

ESP32-S3 TRM (Version 1.7)