**Title: Chapter 12 Timer Group (TIMG)**

---

### Register 12.10, TIMG_WDTCONFIGO_REG (0x0048)

| Bit/Field | Name                          |
|-----------|-------------------------------|
| 31       | TIMG_WDT_EN                  |
| ...       | ...                           |
| 6         | TIMG_WDT_CLK_PRESCALE        |

**Description:**

- **TIMG_WDT_APPCPU_RESET_EN:** Reserved. (R/W)
- **TIMG_WDT_PROCPU_RESET_EN:** WDT reset CPU enable. (R/W)
- **TIMG_WDT_FLASHBOOT_MODE_EN:** When set, Flash boot protection is enabled. (R/W)
- **TIMG_WDT_SYS_RESET_LENGTH:** System reset signal length selection.
  - 0: 100 ns
  - 1: 200 ns
  - 2: 300 ns; 3: 400 ns; 4: 500 ns; 5: 800 ns; 6: 1.6 µs; 7: 3.2 µs (R/W)
- **TIMG_WDT_CPU_RESET_LENGTH:** CPU reset signal length selection.
  - 0: 100 ns
  - 1: 200 ns
  - 2: 300 ns; 3: 400 ns; 4: 500 ns; 5: 800 ns; 6: 1.6 µs; 7: 3.2 µs (R/W)
- **TIMG_WDT_STG3:** Stage 3 configuration.
  - 0: off
  - 1: interrupt
  - 2: reset CPU
  - 3: reset system. (R/W)
- **TIMG_WDT_STG2:** Stage 2 configuration.
  - 0: off
  - 1: interrupt
  - 2: reset CPU
  - 3: reset system. (R/W)
- **TIMG_WDT_STG1:** Stage 1 configuration.
  - 0: off
  - 1: interrupt
  - 2: reset CPU
  - 3: reset system. (R/W)
- **TIMG_WDT_STGO:** Stage 0 configuration.
  - 0: off
  - 1: interrupt
  - 2: reset CPU
  - 3: reset system. (R/W)

**TIMG_WDT_EN:** When set, MWDT is enabled.

---

### Register 12.11, TIMG_WDTCONFIG1_REG (0x004C)

| Bit/Field | Name                          |
|-----------|-------------------------------|
| ...       | ...                           |

**Description:**

- **TIMG_WDT_GK_PRESCALE:** Reserved.
- **TIMG_WDT_CLK PRESCALE:** MWDT clock prescaler value. MWDT clock period = MWDT’s clock source period * TIMG_WDT_CLK_PRESCALE.

---

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

Page number at the bottom of each page:
665