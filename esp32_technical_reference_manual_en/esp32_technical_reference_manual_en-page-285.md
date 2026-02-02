**Chapter Title:**
Chapter 14 AES Accelerator (AES)

**Table of Registers Information**

| Name                | Description                                    | Address       | Access |
|---------------------|-------------------------------------------------|---------------|--------|
| AES_TEXT_3_REG     | AES encrypted/decrypted data register 3        | 0x3FF0103C    | R/W    |
| Control/status registers | - AES START REG: AES operation start control register <br> - AES IDLE REG: AES idle status register | - AES START REG (WO): 0x3FF01000 WO<br>- AES IDLE REG (RO): 0x3FF01004 RO |
| Control/status registers | - AES START REG: AES operation start control register <br> - AES IDLE REG: AES idle status register | - AES START REG (WO): 0x3FF01000 WO<br>- AES IDLE REG (RO): 0x3FF01004 RO |

**Section Title:**  
14.5 Registers

**Body Text:**
The addresses in parenthesis besides register names are the register addresses relative to the AES base address provided in Table 3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory. The absolute register addresses are listed in Section 14.4 Register Summary.

**Subsection Title:**  
Register 14.1. AES_START_REG (0x000)

**Body Text:**
AES_START Write 1 to start the AES operation. (WO)  
AES START

**Subsection Title:**  
Register 14.2. AES_IDLE_REG (0x004)

**Body Text:**
AES IDLE register. Reads 'zero' while the AES Accelerator is busy processing; reads 'one' otherwise. (RO)

**Subsection Title:**  
Register 14.3. AES_MODE_REG (0x008)

**Body Text:**
AES MODE Selects the AES accelerator mode of operation. See Table 14.3-1 for details. (R/W)

**Footer Information:**
Espressif Systems  
285 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback