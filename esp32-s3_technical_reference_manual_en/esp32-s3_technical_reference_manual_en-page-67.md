**Title: Chapter 1 Processor Instruction Extensions (PIE)**

---

| Instruction | QX/QU/QS | Addressing Mode | Register | Description |
|-------------|---------|-----------------|----------|------------|
| EE.FFT.CMUL.S16.ST.XP | qx 1, qy 1, qv 2, as 1, ad 1 | SAR 1 | — | |
| EE.FFT.R2BF.S16 | qx 1, qy 1 | qao0 1, qal1 1 | — | |
| EE.FFT.R2BF.S16.ST.INCP | qx 1, qy 1, as 1 | qao0 1, as 1 | — | |
| EE.FFTVST.R32.DECP | qv 2, as 1 | as 1 | — | |
| EE.GET_GPIO_IN | — | au 1 | GPIO_IN_1 | |
| EE.LD.128.USAR.IP | as 1 | qu 2, as 1 | — | SAR_BYTE_1 |
| EE.LD.128.USAR.XP | as 1, ad 1 | qu 2, as 1 | — | SAR_BYTE_1 |
| EE.LD.ACCX.IP | as 1 | as 1 | ACCX_2 | |
| EE.LD.QACC_H.H.32.IP | as 1 | QACC_H_1 | QACC_H_2 | |
| EE.LD.QACC_H.L.128.IP | as 1 | QACC_H_1 | QACC_H_2 | |
| EE.LD.QACC_L.H.32.IP | as 1 | QACC_L_1 | QACC_L_2 | |
| EE.LD.QACC_L.L.128.IP | as 1 | QACC_L_1 | QACC_L_2 | |
| EE.LD.UA_STATE.IP | as 1 | — | UA_STATE_2 | |
| EE.LDF.128.IP | as 1 | fu3 2, fu2 2, fu1 2, fu0 2, as 1 | QACC_L_2, QACC_H_2 | |
| EE.LDF.128.XP | as 1, ad 1 | fu3 2, fu2 2, fu1 2, fu0 2, as 1 | — | |
| EE.LDF.64.IP | as 1 | fu1 2, fu0 2, as 1 | QACC_L_2, QACC_H_2 | |
| EE.LDF.64.XP | as 1, ad 1 | fu1 2, fu0 2, as 1 | — | |
| EE.LDQA.S16.128.IP | as 1 | as 1 | QACC_L_2, QACC_H_2 | |
| EE.LDQA.S16.128.XP | as 1, ad 1 | as 1 | QACC_L_2, QACC_H_2 | |
| EE.LDQA.S8.128.IP | as 1 | — | QACC_L_2, QACC_H_2 | |
| EE.LDQA.S8.128.XP | as 1, ad 1 | as 1 | QACC_L_2, QACC_H_2 | |
| EE.LDQA.U16.128.IP | as 1 | — | QACC_L_2, QACC_H_2 | |
| EE.LDQA.U16.128.XP | as 1, ad 1 | as 1 | QACC_L_2, QACC_H_2 | |
| EE.LDQA.U8.128.IP | as 1 | — | QACC_L_2, QACC_H_2 | |
| EE.LDQA.U8.128.XP | as 1, ad 1 | as 1 | QACC_L_2, QACC_H_2 | |
| EE.LDXQ.32 | qs 1, as 1 | qu 2 | — | |
| EE.MOV.S16.QACC | qs 1 | — | QACC_L_1, QACC_H_1 | |
| EE.MOV.S8.QACC | qs 1 | — | QACC_L_1, QACC_H_1 | |
| EE.MOV.U16.QACC | qs 1 | — | QACC_L_1, QACC_H_1 | |

---

*Espressif Systems*

*ESP32-S3 TRM (Version 1.7)*

[Submit Documentation Feedback](#)