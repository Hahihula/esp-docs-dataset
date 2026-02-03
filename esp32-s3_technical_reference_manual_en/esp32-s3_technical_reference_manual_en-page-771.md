```markdown
### Title: Chapter 15 Permission Control (PMS)

---

#### Section Header:
- **Register 15.60. PMS_CORE_O_REGION_PMS CONSTRAINT REG (n: 3 - 14)**
  - Address: `0x016C + 4*n`
  
##### Description:
- **Field:** `PMS CORE O REGION PMS CONSTRAINT ADDR O`
  - **Description:** Configures the starting address of Region 0 for CPU. (R/W)
  - **Bit Positions and Values**:
    - Bits: 3, 29
    - Values: 1

##### Field:
- **Field:** `PMS CORE O PIF PMS MONITOR O REG`
  - Address: `0x019C`

##### Description for Register 15.61.
- **Field:** `PMS CORE O PIF PMS MONITOR LOCK`
  - Set this bit to lock CPUO’s PIF interrupt configuration. (R/W)
  - **Bit Positions and Values**:
    - Bits: 3, 0
    - Values: 1

---

#### Footer Information:
- Document version information is present but not fully visible.
```