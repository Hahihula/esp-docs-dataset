**Title: Chapter 1 Processor Instruction Extensions (PIE)**

**Subtitle: GoBack**

---

### **1.6.10 Processor Control Instructions**

As illustrated in Section [1.5.1,2](#), there are various special registers inside the ESP32-S3 processor. In order to facilitate the read and write of the values in such special registers, the following types of processor control instructions are provided to realize the data transfer between the special registers and the AR registers.

- **RSR.* (Read Special register)**
  Can read the value from special registers that come with the processor to the AR register. "* stands for special registers, which only include the SAR register.
  
- **WSR.* (Write Special register)**
  Can modify the value in special registers that come with the processor via the AR register. "*" stands for special registers, which only include the SAR register.

- **XSR.* (Exchange Special register)**
  Can exchange the values inside the AR register and special registers. "*" stands for special registers, which only include the SAR register.
  
- **RUR.* (Read User-defined register)**
  Can read the value from user-defined special registers in the processor to the AR register. "*" stands for special registers, which include SAR_BYTE, ACCX, QACC_H, QACC_L, FFT_BIT_WIDTH and UA_STATE registers.

- **WUR.* (Write User-defined register)**
  Can modify the value in user-defined special registers via the AR register. "* stands for special registers, which include SAR_BYTE, ACCX, QACC_H, QACC_L, FFT_BIT_WIDTH and UA_STATE registers.
  
For special registers that exceed 32-bit width, the "_n" suffix is used to distinguish the instructions that read or write different 32-bit segments from the same special register. Taking reading data from the ACCX register as an example, there are two RUR.* instructions, namely RUR.ACCX_0 and RUR.ACCX_1. The former reads the lower 32-bit data from the ACCX register and write it to the AR register; the latter read the left higher 8-bit data from the ACCX register, perform zero extension and write the result to the AR register. Accordingly, QACC_H and QACC_L registers realize data transfer via the five AR registers.

---

**Footer:**
Espressif Systems  
64  
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)