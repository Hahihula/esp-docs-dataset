**Chapter Title:**
Chapter 11 System Timer (SYSTIMER)

**GoBack Link:** GoBack

---

### Register Section:

#### Register Name and Address:
- **Register 11.2. SYSTIMER_UNITO_OP_REG (0x0004)**

| Bit | Description |
|-----|-------------|
| 31 to 28 | Reserved |

**Description:**
SYSTIMER_TIMER_UNITO_VALUE_VALID UNITO value is synchronized and valid.

- **Access Mode:** Read/SS/WTC
- **Function:** SYSTIMER_TIMER_UNITO_UPDATE Update timer UNITO, i.e., read the UNITO count value to SYS-TIMER_TIMER_UNITO_VALUE_HI and SYSTIMER_TIMER_UNITO_VALUE_LO. (WT)

---

#### Register Name and Address:
- **Register 11.3. SYSTIMER_UNITO_LOAD_HI_REG (0x000C)**

| Bit | Description |
|-----|-------------|
| 29 to 20 | Reserved |

**Description:**
SYSTIMER_TIMER_UNITO_LOAD_HI The value to be loaded to UNITO, high 20 bits.

- **Access Mode:** Read/Write
- **Function:** SYSTIMER_TIMER_UNITO_LOAD_HI

---

#### Register Name and Address:
- **Register 11.4. SYSTIMER_UNITO_LOAD_LO_REG (0x0010)**

| Bit | Description |
|-----|-------------|
| 29 to 0 | Reserved |

**Description:**
SYSTIMER_TIMER_UNITO_LOAD_LO The value to be loaded to UNITO, low 32 bits.

- **Access Mode:** Read/Write
- **Function:** SYSTIMER_TIMER_UNITO_LOAD_LO

---

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback  

**Document Version and Title:**
ESP32-S3 TRM (Version 1.7)