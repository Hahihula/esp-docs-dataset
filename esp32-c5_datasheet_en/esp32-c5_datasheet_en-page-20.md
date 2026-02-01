**Title:**
2 Pins

**Table Title (Top Left):**
Table 2-3 IO MUX Pin Functions shows the IO MUX functions of IO pins.

**Table Header (Top Right):**
Table 2-3. IO MUX Pin Functions

| Pin No. | IO MUX/ GPIO Name^1, 2 | I/O Type | I/MUX Function ^1, 2 | Type |
|---------|------------------------|---------|-----------------------|------|
|         |                        |         |                       |      |

**Table Content:**
- **Row:** 9
  - **IO MUX/ GPIO Name^1, 2:** GPIO00
  - **I/O Type:** GPIO00
  - **I/MUX Function ^1, 2:** I/O/T
  - **Type:** I/O/T

- ... (similar rows for other pins)

**Footnotes:**
1. Bold marks the default pin functions in the default boot mode. See Section 3.1 Chip Boot Mode Control.
2. Regarding highlighted cells, see Section 2.4 Restrictions for GPIOs and LP GPIOs.

**Additional Information at Bottom of Page (in italics):**
Each IO MUX function (Fn, n = 0 ~ 2) is associated with a type. The description of type is as follows:
- I – input.
- O – output.
- T – high impedance.
- Il – input; if the pin is assigned a function other than Fn, the input signal of Fn is always 1.

**Additional Information at Bottom (continued):**
IO – input; if the pin is assigned a function other than Fn, the input signal of Fn is always Ø. 

**Footer:**
Espressif Systems
20
Submit Documentation Feedback

**Document Title and Version Note in Footer:**
ESP32-C5 Series Datasheet v1.0