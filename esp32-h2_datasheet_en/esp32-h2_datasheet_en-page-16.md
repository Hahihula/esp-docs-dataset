**Title: Pins**

---

**Table Title:** Table 2-3 – cont’d from previous page

**Subtitle:** IO MUX Function, 1, 2, 3

| Pin No. | IO MUX / GPIO Name^2 | F0 Type | F1 Type | F2 Type | F3 Type | F4 Type |
|---------|-----------------------|--------|--------|--------|--------|--------|
| 11      | GPIO9                 | I/O/T   | GPIO9  | I/O/T   |        |        |
| 12      | GPIO10                | I/O/T   | GPIO10 | I/O/T   |        |        |
| 13      | GPIO11                | I/O/T   | GPIO11 | I/O/T   |        |        |
| 14      | GPIO12                | I/O/T   | GPIO12 | I/O/T   |        |        |
| 15      | GPIO13                | I/O/T   | GPIO13 | I/O/T   |        |        |
| 16      | GPIO14                | I/O/T   | GPIO14 | I/O/T   |        |        |
| 21      | GPIO22                | I/O/T   | GPIO22 | I/O/T   |        |        |
| 22      | UORXD                 | I1     | GPIO23 | FSPICS1 | O/T    |        |
| 23      | GPIO24                |       |       | FSPICES2| O/T    |        |
| 24      | GPIO25                | O      | GPIO25 | FSPICES3| O/T    |        |
| 25      | GPIO26                | I/O     | GPIO26 | FSPICES4 | O/T   |        |
| 26      | GPIO27                | I/O/T   | GPIO27 | I/O/T   | FSPICS5 | O/T    |

**Footnotes:**
1. Bold marks the default pin functions in the default boot mode. See Section 3.31 Chip Boot Mode Control.
2. Regarding highlighted cells, see Section [2.3.3 Restrictions for GPIOs](#).
3. Each IO MUX function (Fn, n = 0 ~ 4) is associated with a type.

**Description of Type:**
- I – input
- O – output
- T – high impedance

**Additional Notes on Pin Functionality:**
- If the pin assigned to a function other than Fn, the input signal of Fn is always 1.
- IO – input; if the pin is assigned as a function other than Fn, the input signal of Fn is always 0.

---

**Footer:**  
Espressif Systems  
ESP32-H2 Series Datasheet v1.2

**Link:** Submit Documentation Feedback