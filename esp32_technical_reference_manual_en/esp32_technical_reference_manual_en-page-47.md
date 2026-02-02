**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Section Heading:**
1.8 Registers

**Subsection Heading and Content:**
1.8.1 SENS_ULP Address Space

The addresses in parenthesis besides register names are the register addresses relative to (the RTC base address + 0x0800). The RTC base address is provided in Table 3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory. The absolute register addresses are listed in Section 1.7.1 SENS_ULP Address Space.

**Diagram Description:**
- **Register 1.1:** SENS_ULP_CP_SLEEP_CYCn_REG (n: 0-4) (0x18+0x4*n)
  - A binary representation of the register with bits labeled from n to Reset.
  
- **Register 1.2:** SENS_SAR_START FORCE REG (0x002c)
  - Binary diagram showing specific bit positions and their labels, such as SENS_ULP_CP_START_TOP, SENS_PC_INIT, etc.

**Text Description:**
SENS_ULP_CP_SLEEP_CYCn_REG
- ULP timer cycles setting n; the ULP coprocessor can select one of such registers by using the SLEEP instruction. (R/W)

Register 1.2:
- **SENS_SAR_START FORCE REG (0x002c)**
  - Binary diagram with specific bit positions and their labels.
  
**Text Description:**
SENS_PC_INIT
- ULP PC entry address. (R/W)
  
SENS_ULP_CP_START_TOP
- Set this bit to start the ULP coprocessor; it is active only when SENS_ULP_CP FORCE START_TOP = 1. (R/W)

SENS_ULP_CP FORCE START_TOP:
- ULP coprocessor is started by SENS_ULP_CP START TOP: 0: ULP coprocessor is started by timer.

**Footer Information:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback