**Chapter Title:**
Chapter 7 Reset and Clock

**GoBack Link:** GoBack

---

**Section Header (Register):**
Register 7.4. SYSCON_CK8M_TICK_CONF_REG (0x00C)

**Binary Representation Diagram for Register 7.4:**

```
0 1 2 3 4 5 6 7
|              |
+-------------+
|             |
|    Reset     |
|             |
+-------------+
```

**Description of Register 7.4:**
SYSCON_CK8M_TICK_NUM Configures the divider value of REF_TICK when the source of APB_CLK is FOSC_CLK. The value range is 0x0 ~ 0xFF. REF_TICK = APB_CLK / (the value of this field + 1).
(R/W)

---

**Section Header (Register):**
Register 7.5. SYSCON_APLL_TICK_CONF_REG (0x003C)

**Binary Representation Diagram for Register 7.5:**

```
0 1 2 3 4 5 6 7
|              |
+-------------+
|             |
|    Reset     |
|             |
+-------------+
```

**Description of Register 7.5:**
SYSCON_APLL_TICK_NUM Configures the divider value of REF_TICK when the source of APB_CLK is APLL_CLK. The value range is 0x0 ~ 0xFF. REF_TICK = APB_CLK / (the value of this field + 1).
(R/W)

---

**Section Header (Register):**
Register 7.6. SYSCON_DATE_REG (0x007C)

**Binary Representation Diagram for Register 7.6:**

```
0 1 2 3 4 5 6 7
|              |
+-------------+
|             |
|    Reset     |
|             |
+-------------+
```

**Description of Register 7.6:**
SYSCON_DATE Chip revision register. For more information see ESP32 Series SoC Errata.
(R/W)

---

**Footer Information:** 
Espressif Systems
173
ESP32 TRM (Version 5.6)
Submit Documentation Feedback