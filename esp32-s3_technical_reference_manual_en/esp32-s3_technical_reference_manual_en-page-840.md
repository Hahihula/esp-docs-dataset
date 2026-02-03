**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**Section Header:**
Register 17.20. SYSTEM_SYSLCK_CONF_REG (0x060)

**Binary Representation and Description of Register:**
```
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
| 31 | 19 | 18 | ... | 12 | 11 | 10 | 9 | 8 |
+----+-----+-----+-----+-----+-----+-----+-----+
|     |     |     |     |     |     |     |     |
+----+-----+-----+-----+-----+-----+-----+-----+
```
- **SYSTEM_PRE_DIV_CNT**: This field is used to set the count of prescaler of XTAL_CLK. For details, please refer to Table 7.2-3 in Chapter 7 Reset and Clock (R/W).

**Section Header:**
Register 17.21. SYSTEM_DATE_REG (0x0FFC)

**Binary Representation and Description of Register:**
```
0 0 0 0
| 31 | 28 | 27 | ... |
+----+-----+-----+-----+
|     |     |     |     |
+----+-----+-----+-----+
```
- **SYSTEM_DATE**: Version control register (R/W).

**Section Header:**
Register 17.22. SYSCON_CLKGATE FORCE_ON_REG (0x00A8)

**Binary Representation and Description of Register:**
```
0 0 0 0
| 31 | ... |
+----+-----+
|     |     |
+----+-----+
```
- **SYSCON_ROM_CLKGATEFORCE_ON**: Set 1 to configure the ROM clock gate to be always on; set 0 to configure the clock gate to turn on automatically when ROM is accessed and turn off automatically when ROM is not accessed (R/W).
  
- **SYSCON_SRAM_CLKGATEFORCE_ON**: Set 1 to configure the SRAM clock gate to be always on; set 0 to configure the clock gate to turn on automatically when SRAM is accessed and turn off automatically when SRAM is not accessed (R/W).

**Footer:**
Espressif Systems
840 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback