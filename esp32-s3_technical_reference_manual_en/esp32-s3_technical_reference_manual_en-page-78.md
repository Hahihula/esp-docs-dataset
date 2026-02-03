**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Body Text:**

```
36    qa[95:80] = {6'h0, max(tmp5[9:0], Switch10(tmp5[9:0]))}
37    qa[111:96] = {6'h0, max(tmp6[9:0], Switch10(tmp6[9:0]))}
38    qa[127:112] = {6'h0, max(tmp7[9:0], Switch10(tmp7[9:0]))}
40    as[31:0] = as[31:0] + 8
```

**Footer Text:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**  
ESP32-S3 TRM (Version 1.7)