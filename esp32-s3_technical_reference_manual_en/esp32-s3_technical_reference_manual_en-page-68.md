**Title: Chapter 1 Processor Instruction Extensions (PIE)**

**GoBack**

| Instruction Code | Description | Source Register(s) | Destination Register(s) | Addressing Mode | Memory/Peripheral Access |
|-------------------|-------------|---------------------|---------------------------|-----------------|--------------------------|
| EE.MOV.U8.QACC    | Move 8-bit value from QACC to a register. | qs1 | — | QACC_L, 1 | — |
| EE.MOVI.32.A      | Move immediate value into A. | qs 1 | au 1 | — | — |
| EE.MOVI.32.Q      | Move immediate value into Q. | as 1 | qu 1 | — | — |
| EE.NOTQ           | Negate the contents of a register or memory location and store it in another register or memory location, depending on the condition code set by the previous instruction (if). | qx 1 | qa 1 | — | — |
| EE.ORG            | One-byte OR operation between two registers/memories. | qx 1, qy 1 | qa 1 | — | — |
| EE.SET_BIT_GPIO_OUT | Set a bit in GPIO_OUT register to the specified value (0 or 1). | qs1, qsO 1 | qs1, qsO 1 | GPIO_OUT_1 | GPIO_OUT_1 |
| EE.SLCI.2Q        | Select and copy two registers into Q. | qs1, qsO 1 as 1, ad 1 | qs1, qsO 1 as 1 | — | — |
| EE.SRC.Q          | Move a register or memory location to SRC. | qs0 1, qs1 1 | qa 1 | SAR_BYTE_1 | — |
| EE.SRC.Q.LD.IP     | Load immediate value into SRC. | as 1, qsO 1, qs1 1 | qu 2, as 1, qsO 1 | SAR_BYTE_1 | — |
| EE.SRC.Q.LD.XP     | Load a register or memory location to SRC. | as 1, ad 1, qs0 1 | qu 2, as 1, qsO 1 | SAR_BYTE_1 | — |
| EE.SRC.Q.QUP       | Move a register from QUP to SRC. | qs0 1, qs1 1 | qa 1, qsO 1 | SAR_BYTE_1 | — |
| EE.SRCI.2Q        | Select and copy two registers into CIR. | qs1 1, qsO 1 | qs1 1, qsO 1 | QACC_H, 1 | QACC_H, 1 |
| EE.SRCMB.S16.QACC | Move a register or memory location to SRCMB. | as 1 | qu 1 | QACC_L_1 | QACC_L_1 |
| EE.SRCMB.S8.QACC  | Select and copy two registers into CIR. | as 1 | qu 1 | QACC_H, 1 | QACC_H, 1 |
| EE.SRCQ.128.ST.INCP | Move a register or memory location to SRCQ. | qsO 1, qs1 1 as 1, ad 1 | qs1, qsO 1 as 1 | SAR_BYTE_1 | — |
| EE.SRCXXP.2Q      | Select and copy two registers into CIR. | qs1 1, qsO 1 as 1, ad 1 | qs1 1, qsO 1 as 1 | ACCX_1 | ACCX_1 |
| EE.SRS.ACCX       | Move a register or memory location to SRCMB. | as 1 | au 1 | — | — |
| EE.ST.ACCX.IP     | Load immediate value into ST. | as 1 | as 1 | ACCX_1 | — |
| EE.ST.QACC_H.H.32.IP | Move a register or memory location to QACC_H. | as 1 | as 1 | QACC_H, 1 | — |
| EE.ST.QACC_H.L.128.IP | Move a register or memory location to QACC_H. | as 1 | as 1 | QACC_H_1 | — |
| EE.ST.QACC_L.H.32.IP | Move a register or memory location to QACC_L. | as 1 | as 1 | QACC_L, 1 | — |
| EE.ST.QACC_L.L.128.IP | Move a register or memory location to QACC_L. | as 1 | as 1 | QACC_L_1 | — |
| EE.ST.UA_STATE.IP | Load immediate value into ST_UA_STATE. | as 1 | as 1 | UA_STATE_1 | — |
| EE.STF.128.IP     | Move a register or memory location to STF. | fv3, fv2, fv1, fv0, as 1 | as 1 | — | — |
| EE.STF.64.IP      | Move a register or memory location to STF. | fv1, fv0, as 1 | as 1 | — | — |
| EE.STF.64.XP      | Select and copy two registers into CIR. | fv1, fv0, as 1, ad 1 | as 1 | — | — |
| EE.STXQ.32        | Move a register or memory location to STXQ. | qv 1, qs 1, as 1 | — | — | — |
| EE.VADDS.S16      | Add two registers and store the result in another register/mem location (if). | qx 1, qy 1 | qa 1 | — | — |
| EE.VADDS.S16.LD.INCP | Load immediate value into VADDS. | as 1, qsO 1, qs1 1 | qu 2, as 1, qsO 1 | QACC_L_1 | — |
| EE.VADDS.S16.ST.INCP | Move a register or memory location to VADDS. | as 1, qsO 1, qs1 1 | qu 2, as 1, qsO 1 | ACCX_1 | ACCX_1 |
| EE.VADDS.S32      | Add two registers and store the result in another register/mem location (if). | qx 1, qy 1 | qa 1 | — | — |
| EE.VADDS.S32.LD.INCP | Load immediate value into VADDS. | as 1, qsO 1, qs1 1 | qu 2, as 1, qsO 1 | QACC_H_1 | QACC_H_1 |

**Footer:**
Espressif Systems  
68 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback