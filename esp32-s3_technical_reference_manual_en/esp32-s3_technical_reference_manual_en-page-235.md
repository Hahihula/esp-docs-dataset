**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Body Text:**

```
QACC_H[159:140] = min(max(QACC_H[159:140] + qx[127:120] * qy[127:120], -2^{19}), 2^{19}-1)

qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + ad[31:0]
qsθ[127:0] = {qs1[127:0], qsθ[127:0]} >> {SAR_BYTE[3:0] << 3}
```

**Footer Text:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)