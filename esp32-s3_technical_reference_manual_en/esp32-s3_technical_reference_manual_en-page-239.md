**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Body Text:**

```
QACC_H[159:140] = min(max(QACC_H[159:140] + qx[127:120] * qy[127:120], -2^{19}), 2^{19}-1)

qu[127:0] = {16<load8(as[31:0])}}

as[31:0] = as[31:0] + 1

qsθ[127:0] = {qs1[127:0], qsθ[127:0]} >> {SAR_BYTE[3:0] << 3}
```

**Footer Information:**
Espressif Systems
Page Number: 239
Document Title: ESP32-S3 TRM (Version 1.7)
Link Texts:
- Submit Documentation Feedback

**Navigation Link:**
GoBack