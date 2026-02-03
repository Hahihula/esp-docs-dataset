**Title: Chapter 1 Processor Instruction Extensions (PIE)**

---

| Command | Description | QACC_H | QACC_L |
|---------|-------------|--------|--------|
| EE.VMULAS.S16.QACC.LD.XP | as 1, ad 1, qx 1, qy 1 | qu 2, as 1 | QACC_H 2, QACC_L 2 |
| EE.VMULAS.S16.QACC.LD.XP.QUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, QACC_L 2 |
| EE.VMULAS.S16.QACC.LDBC.INC.P | as 1, qx 1, qy 1 | qu 2, as 1 | QACC_H 2, QACC_L 2 |
| EE.VMULAS.S16.QACC.LDBC.INC.P QUUP | as 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | SAR_BYTE 1, QACC_H 2, QACC_L 2 |
| EE.VMULAS.S8.ACCX | qx 1, qy 1 | — | ACCX 2 |
| EE.VMULAS.S8.ACCX.LD.IP | as 1, qx 0, qs0 1, qs1 1 | qu 2, as 1 | ACCX 2 |
| EE.VMULAS.S8.ACCX.LD.IP.QUUP | as 1, qx 1, qy 1, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | SAR_BYTE 1, ACCX 2 |
| EE.VMULAS.S8.ACCX.LD.XP | as 1, ad 1, qx 1, qy 1 | qu 2, as 1 | ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 2 |
| EE.VMULAS.S8.ACCX.LDBC.INC.PQUUP | as 1, ad 1, qx 0, qs0 1, qs1 1 | qu 2, as 1, qs0 1 | QACC_H 2, ACCX 