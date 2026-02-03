**Title: Chapter 1 Processor Instruction Extensions (PIE)**

---

### Figure Caption:
- **Figure 1.7-1**: Interlock Caused by Instruction Operand Dependency

### Diagram Description:

The diagram illustrates the interlock caused due to instruction operand dependency in a processor pipeline.

- The cycle is divided into multiple stages: T0, T+1, T+2, etc.
- Instructions A and B are shown progressing through different states (I for In-flight, R for Ready).
- Instruction A was over with resulting write operation being written back from register X to the next stage in sequence.

### Text Description:
Data dependencies between instructions are determined by the dependencies between operands and pipeline stages at which reads and writes happen. Table 1.7-2 lists all operands of the ESP32-S3 extended instructions, including implicit special register write (def) and read (use) pipeline stage information.


---

### Table Caption:

**Table 1.7-2**: Extended Instruction Pipeline Stages

| Instruction | Operand Pipeline Stage Use | Def | Special Register Pipeline Stage Use | Def |
|-------------|---------------------------|-----|--------------------------------------|-----|
| EE.ANDQ     | qx 1, qy 1               | qa 1 |                                    |     |
| EE.BITREV    | ax 1                     | qa 1, ax 1              FFT_BIT_WIDTH | —   |
| EE.CLR_BIT_GPIO_OUT | — | GPIO_OUT 1 | GPIO_OUT 1 | — |
| EE.CMUL.S16 | qx 1, qy 1               | qz 2 | SAR 1 | — |
| EE.CMUL.S16.LD.INCP | as 1, qx 1, qy 1       | qu 2, as 1, qx 2      | SAR 1 | — |
| EE.CMUL.S16.ST.INCP | qx 2, as 1, qx 1        | as 1, qx 2            | SAR 1 | — |
| EE.FFT.AMS.S16.LD.INCP | qx 1, qy 1               | qu 2, as 1, qx 2      | SAR 1 | — |
| EE.FFT.AMS.S16.LD.INCP.UAUP | qx 1, qy 1              | qu 2, as 1, qx 2      | SAR_BYTE | UA_STATE 1 |
| EE.FFT.AMS.S16.LD.R32.DECP | qx 1, qy 1               | qu 2, as 1, qx 2      | SAR 1 | — |
| EE.FFT.AMS.S16.ST.INCP | qx 1, qy 1               | qz1 2, as0 1, as       | SAR 1 | — |
| EE.FFT.CMUL.S16.LD.XP | as 1, ad 1, qx 1        | qu 2, as 1, qx 2      | SAR 1 | — |

---

**Footer:**
- Espressif Systems
- Page number: 66
- Document version and title: ESP32-S3 TRM (Version 1.7)