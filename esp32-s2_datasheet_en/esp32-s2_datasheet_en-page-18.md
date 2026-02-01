**Title: Pins**

---

**Subtitle: Cont'd from previous page**

**Table: IO MUX Function**

| Pin No. | GPIO | FO   | Type F1 | Type F2  | Type F3    | Type F4     | Type |
|---------|------|------|---------|----------|------------|-------------|------|
| 42      | GPIO38 | GPIO38 | I/O/T   | FSPIWP   | I/O/T      | SUBSPIWP    | I1/O/T |
| 43      | GPIO39 | MTCK | I1      | GPIO39   | I/O/T      | CLK_OUT3    | O     |
|         |       |      |         |          |            | SUBSPCS1    | O/T   |
| 44      | GPIO40 | MTDIO | O/T     | GPIO40   | I/O/T      | CLK_OUT2    | O     |
|         |       |      |         |          |            |             |       |
| 46      | GPIO41 | MTDI | I1      | GPIO41   | I/O/T      | CLK_OUT1    | O     |
|         |       |      |         |          |            |             |       |
| 47      | GPIO42 | MTMS | I0      | GPIO42   | I/O        |             |       |
|         |       |      |         |          |            |             |       |
| 48      | GPIO43 | UOTXD | O/T     | GPIO43   | I/O/T      | CLK_OUT1    | O     |
|         |       |      |         |          |            |             |       |
| 49      | GPIO44 | UORXD | D1      | GPIO44   | I/O/T      | CLK_OUT2    | O     |
|         |       |      |         |          |            |             |       |
| 50      | GPIO45 | GPIO45 | I/O/T   | GPIO45   | I/O/T      |             |       |
|         |       |      |         |          |            |             |       |
| 55      | GPIO46 | GPIO46 | I1      | GPIO46   | I           |             |       |

**Footnotes:**
1. Bold marks the default pin functions in the default boot mode. See Section 3.1 Chip Boot Mode Control.
2. Regarding highlighted cells, see Section 2.3.5 Restrictions for GPIOs and RTC_GPIOs.

**Description of type codes (Fn, n = 0 ~ 4):**
- I – input
- O – output
- T – high impedance

**Additional Information:**
- If the pin is assigned a function other than Fn, the input signal of Fn is always 1.
- IO – input; if the pin is assigned a function other than Fn, the input signal of Fn is always Θ.

---

**Footer:**  
Espressif Systems  
ESP32-S2 Series Datasheet v1.8

Submit Documentation Feedback