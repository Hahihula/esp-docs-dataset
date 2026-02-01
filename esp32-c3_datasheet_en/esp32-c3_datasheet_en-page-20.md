**Title: Pins**

---

### Table-24 – cont’d from previous page

| Pin No. | IO MUX / Name | F0 | Type^3 | F1 | Type | F2 | Type |
|---------|---------------|----|--------|----|------|----|------|
| 5       | GPIO1         | GPIO1 | I/O/T   | GPIO1 | I/O/T |
| 6       | GPIO2         | GPIO2 | I/O/T   | GPIO2 | FSPIQ |
| 8       | GPIO3         | GPIO3 | I/O/T   | GPIO3 | I/O/T |
| 9       | GPIO4 (MTMS)  | MTMS | I1      | GPIO4 | OTHD |
| 10      | GPIO5         | MTDI | I1      | GPIO5 | FSPWP |
| 12      | GPIO6         | MTCK | I1      | GPIO6 | FSPCLK |
| 13      | GPIO7 (MTDO)  | MTDO | O/T     | GPIO7 | I/O/T |
| 14      | GPIO8         | GPIO8 | I/O/T   | GPIO8 | I/O/T |
| 15      | GPIO9         | GPIO9 | I/O/T   | GPIO9 | FSPSO |
| 16      | GPIO10        | GPIO10 | I/O/T  | GPIO10 | I/O/T |
| 18      | GPIO11        | GPIO11 | I/O/T  | GPIO11 | FSPSO |
| 19      | GPIO12 (SPIHD)| SPIHD | I1/O/T | GPIO12 | I/O/T |
| 20      | GPIO13        | SPIWP | I1/O/T | GPIO13 | OTHD |
| 21      | GPIO14        | SPICSO | O/T    | GPIO14 | I/O/T |
| 22      | GPIO15 (SPICLK)| SPICLK | I1/O/T | GPIO15 | FSPWP |
| 23      | GPIO16        | SPID | I1/O/T  | GPIO16 | OTHD |
| 24      | GPIO17        | SPIQ | I1/O/T  | GPIO17 | I/O/T |
| 25      | GPIO18        | GPIO18 | I/O/T   | GPIO18 | FSPCLK |
| 26      | GPIO19        | GPIO19 | I/O/T   | GPIO19 | OTHD |
| 27      | GPIO20 (UORXD)| UORXD | I1     | GPIO20 | I/O/T |
| 28      | GPIO21 (UOTXD)| UOTXD | O       | GPIO21 | FSPSO |

---

**Footnotes:**

1. Bold marks the default pin functions in the default boot mode. See Section **3.1 Chip Boot Mode Control**.
2. Regarding highlighted cells, see Section 2.3.3 Restrictions for GPIOs.

Each IO MUX function (Fn, n = 0 ~ 2) is associated with a type. The description of type is as follows:
- I – input; O – output; T – high impedance;
- If Fn is always assigned to the pin if the pin: the pin signal other than Fn.
- Io – input; if the pin function, the input signal of Fn.

---

**Footer Information:**  
Espressif Systems  
20  
ESP32-C3 Series Datasheet v2.2  

[Submit Documentation Feedback](#)