**Title:**
Chapter 37 Remote Control Peripheral (RMT)

**Subtitle:**
37.6 Registers

**Body Text:**
The addresses in this section are relative to RMT base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Subsection Title:**
Register 371, RMT_CHnDATA_REG (n: 0-3) (0x0000+0x4*n)

**Diagram Description for Register 371:**
```
| 31 | 0 |
|----|---|
|     | Reset
```

**Description under Diagram:**
RMT_CHnDATA Read and write data for channel n via APB FIFO. (RO)

**Subsection Title:**
Register 372, RMT_CHmDATA_REG (m = 4, 5, 6, 7) (0x0010, 0x0014, 0x0018, 0x001C)

**Diagram Description for Register 372:**
```
| 31 | 0 |
|----|---|
|     | Reset
```

**Description under Diagram:**
RMT_CHmDATA Read and write data for channel m via APB FIFO. (RO)

**Footer Information:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback