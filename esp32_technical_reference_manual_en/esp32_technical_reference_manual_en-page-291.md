**Title:**
Chapter 15 RSA Accelerator (RSA)

**Subtitle:**
15.5 Registers

**Body Text:**
The addresses in parenthesis besides register names are the register addresses relative to the RSA base address provided in Table 3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory. The absolute register addresses are listed in Section 15.4 Register Summary.

**Subsection with Diagrams (Register Descriptions):**

1. **Register 15.1: RSA_M_PRIME_REG (0x800)**
   - Description:
     ```
     RSA_M_PRIME_REG
     This register contains M'. (R/W)
     ```
   - Diagram:
     ```
     [31] | [0]
     -------------------
     ```

2. **Register 15.2: RSA_MODEXP_MODE_REG (0x804)**
   - Description:
     ```
     RSA_MODEXP_MODE
     This register contains the mode of modular exponentiation. (R/W)
     ```
   - Diagram:
     ```
     [31] | [2] | [0]
     -------------------
     ```

3. **Register 15.3: RSA_MODEXP_START_REG (0x808)**
   - Description:
     ```
     RSA_MODEXP_START
     Write 1 to start modular exponentiation. (WO)
     ```
   - Diagram:
     ```
     [31] | [1] | [0]
     -------------------
     ```

**Footer:**
Espressif Systems  
291 ESP32 TRM (Version 5.6)  
Submit Documentation Feedback