**Title: Chapter 1 Processor Instruction Extensions (PIE)**

---

### Figure Caption:
- **Figure 1.3-1. PIE Internal Structure (MAC)**

### Diagram Description:

The diagram shows the data flow paths and PIE components.

#### Components of the PIE Unit Include:
- Address unit that reads 8/16/32/64/128-bit aligned data
- Bank of eight 128-bit vector QR registers
- Arithmetic logic unit (ALU) with sixteen 8-bit multipliers, and eight 16-bit multipliers.
- QACC_H/QACC_L - Two 160-bit accumulators
- ACCX - A 40-bit accumulator

---

### Subtitle:
**1.3.1 Bank of Vector Registers**

#### Body Text:

Bank of vector registers contains 8 vector registers (QR). Each register could be represented as an array of 16 x 8-bit data words, or a bank of eight QR registers with sizes chosen from the following formats: 
- Depending on used instructions:
  - 8
  - 16
  - Or

---

**Footer Information:**  
Espressif Systems  
Submit Documentation Feedback  

**Document Version and Reference:**  
ESP32-S3 TRM (Version 1.7)