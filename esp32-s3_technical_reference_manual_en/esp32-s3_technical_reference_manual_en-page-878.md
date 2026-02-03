**Chapter Title:**
Chapter 20 RSA Accelerator (RSA)

**Section Titles and Content:**

---

### **20.4 Memory Summary**

The addresses in this section are relative to the RSA accelerator base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Title:** 
Table 20.4-1. RSA Accelerator Memory Blocks

| Name          | Description                   | Size (byte) | Starting Address | Ending Address | Access |
|---------------|-------------------------------|-------------|------------------|----------------|-------|
| RSA_M_MEM     | Memory M                      | 512         | 0x0000           | 0x01FF         | WO    |
| RSA_Z_MEM     | Memory Z                      | 512         | 0x0200           | 0x03FF         | R/W   |
| RSA_Y_MEM     | Memory Y                      | 512         | 0x0400           | 0x05FF         | WO    |
| RSA_X_MEM     | Memory X                      | 512         | 0x0600           | 0x07FF         | WO    |

---

### **20.5 Register Summary**

The addresses in this section are relative to the RSA accelerator base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

**Table Title:** 
Configuration Registers

| Name          | Description                   | Address       | Access |
|---------------|-------------------------------|---------------|--------|
| RSA_M_PRIME_REG   | Register to store M'         | 0x800         | R/W    |
| RSA_MODE_REG     | RSA length mode               | 0x804         | R/W    |
| RSA_CONSTANT_TIME_REG | The constant_time option      | 0x820         | R/W    |
| RSA_SEARCH_ENABLE_REG | The search option             | 0x824         | R/W    |
| RSA_SEARCH_POS_REG   | The search position           | 0x828         | R/W    |

**Status/Control Registers**

| Name          | Description                   | Address       | Access |
|---------------|-------------------------------|---------------|--------|
| RSA_CLEAN_REG     | RSA clean register             | 0x808         | RO     |
| RSA_MODEEXP_START_REG | Modular exponentiation starting bit | 0x80C   | WO     |
| RSA_MODMULT_START_REG | Modular multiplication starting bit | 0x810    | WO     |
| RSA_MULT_START_REG   | Normal multiplication starting bit | 0x814   | WO     |
| RSA_IDLE_REG      | RSA idle register              | 0x818         | RO     |

**Interrupt Registers**

| Name          | Description                   | Address       | Access |
|---------------|-------------------------------|---------------|--------|
| RSA_CLEAR_INTERRUPT_REG | RSA clear interrupt register    | 0x81C         | WO     |
| RSA_INTERRUPT_ENA_REG   | RSA interrupt enable register   | 0x82C         | R/W    |

**Version Register**

| Name          | Description                   | Address       | Access |
|---------------|-------------------------------|---------------|--------|
| RSA_DATE_REG      | Version control register      | 0x830         | R/W    |

---

### **20.6 Registers**

The addresses in this section are relative to the RSA accelerator base address provided in Table 4.3-3 in Chapter 4 System and Memory.

**Footer:**
Espressif Systems  
Page number: 878  
Document version (Version 1.7)  

[Submit Documentation Feedback](#)