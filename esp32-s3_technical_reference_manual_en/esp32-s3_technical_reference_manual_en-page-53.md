**Title: Chapter 1 Processor Instruction Extensions (PIE)**

---

### Table of Contents:
- **Instruction Type**
  - Shift instructions
    - EE.SRC.Q
    - EE.SRC.Q.GUP
    - EE.SRC.Q.LD.[XP/IP]
    - EE.SLCI.2Q
    - EE.SLCXXP.2Q
    - EE.SRCI.2Q
    - EE.SRCXXP.2Q
    - EE.SRCQ.128.ST.INCP
    - EE.VSR.32
    - EE.VSL.32
    - EE.FFT.R2BF.S16.[7-ST.INCP]
    - EE.FFT.CMUL.S16.[LD.XP/ST.XP]
  - FFT dedicated instructions
    - EE.BITREV
    - EE.FFT.AMS.S16.[LD.INCUPAUF/LD.INCUP.LDR32.DECP/ST.INCP]
    - EE.FFT.VST.R32.DECP
  - GPIO control instructions
    - EE.WR_MASK_GPIO_OUT
    - EE.SET_BIT_GPIO_OUT
    - EE.CLR_BIT_GPIO_OUT
    - EE.GET_GPIO_IN
  - Processor control instructions
    - RSR.*
    - WSR.*
    - XSR.*
    - RUR.*
    - WUR.*

---

**Reference Section:**
- Shift instructions (1.6.7)
- FFT dedicated instructions (1.6.8)
- GPIO control instructions (1.6.9)
- Processor control instructions (1.6.10)

---

### Subtitle:
**1.6.1 Read Instructions**

**Body Text:**
Read instructions tell the processor to issue a virtual address to access memory based on the AR register that stores access address information. Most read instructions read memory first, and then update the access address.
EE.LDXQ.32 is a special case where the instruction first selects a piece of 16-bit data in the QR register via an immediate value, adds it to the access address, and then issues the access operation.

Since access to non-aligned addresses will cause slower response, all virtual addresses issued by read instructions in the extended instruction set are forced to be aligned according to data formats. Depending on the size of the access data format, corresponding length of data will be returned by memory as 1-byte, 2-byte, 4-byte, 8-byte or 16-byte. When the data read after forced alignment is not as expected, the desired data can be extracted from multiple QR registers using instructions such as EE.SRC.Q.

The table below briefly describes the access operations performed by read instructions. For detailed information about read instructions, please see Section 1.8

---

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback