**Title: Chapter 15 Permission Control (PMS)**

---

### Register Information:

- **Register 15.107**: `SYSCON_SRAM_ACEN_SIZE_REG`
  - Description: Configure the length of SRAM Region n.
  - Size should be aligned to 64 KB.

#### Address:
- Offset in address space (n): 0x0078 + 4*n

#### Bits and Values:
- Bit positions from left-to-right are labeled as follows, with bit numbers on top: `31`, `16`, `15`, `...`, `0`
- Example value shown is `0x1000`

---

### Register Information:

- **Register 15.108**: `SYSCON_SPI_MEM_PMS_CTRL_REG`
  - Offset in address space: 0x0088

#### Bits and Values:
- Bit positions from left-to-right are labeled as follows, with bit numbers on top (in parentheses): `31`, `...`, `2`, `1`, `0`
- Example value shown is `0x0`

---

### Registers:

- **SYSCON_SRAM_ACEN_SIZE**  
  - Description: Configure the length of SRAM Region n. The size should be aligned to 64 KB.

- **SYSCON_SPI_MEM_REJECT_CODE**
  - Description (RO): Indicates exception accessing external memory and triggers an interrupt.
  - Values include invalid region, overlapping regions, illegal write, illegal read, etc., as described in the document feedback section on page `799`.

- **SYSCON_SPI_MEM_REJECT_CLR**  
  - Description: Set this bit to clear the exception status.

- **SYSCON_SPI_MEM_REJECT_CDE**
  - Description (RO): Stores the exception cause.
  - Values include invalid region, overlapping regions, illegal write, etc., as described in detail on page `799`.

---

**Navigation Links:**  
- [Go Back](#)  

**Document Version: ESP32-S3 TRM (Version 1.0)**

**Feedback Link:** Submit Documentation Feedback