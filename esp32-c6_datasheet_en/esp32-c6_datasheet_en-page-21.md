**Title:**
2 Pins

**Table Title:**
Table 2-5. QFN32 IO MUX Pin Functions

**Table Columns and Headers:**
1. **Pin No.:** GPIO0, GPIO1, GPIO2,..., GPIO28.
2. **IO MUX / FO Name:** GPIO0, GPIO1, GPIO2,..., GPIO27 (GPIO24 highlighted as "highlighted" in the document).
3. **IO MUX Function 1, 2, 3 Type F0:**
   - I/O/T
   - I/O/T
   - I/O/T
   - ...
4. **IO MUX Function 1 Type F1:**
   - GPIO0/I/O/T
   - GPIO1/I/O/T
   - GPIO2/I/O/T
   - ...
5. **IO MUX Function 2 Type F2:**
   - I/O/T
   - FSPIQ
   - I/O/T
   - ...
6. **IO MUX Function 3 Type (last column):**
   - II/O/T

**Highlighted Pins in the Table:** 
- GPIO15, GPIO24 are highlighted.

**Footnotes:**
1. Bold marks the default pin functions in the default boot mode.
2. Regarding "highlighted" cells see Section 3.4 Restrictions for GPIOs and LP GPIOs
3. Each IO MUX function (Fn, n = 0 ~ 2) is associated with a type.

**Legend:**
- I – input; O – output; T – high impedance.
- If the pin signal of Fn is always 1 or if the pin assigned to other than Fn functions has an unspecified value for Fn. 

**Additional Information in Footnotes and Table:**
- Section references:
   - "Chip Boot Mode Control" (Section not specified).
   - "Restrictions for GPIOs and LP GPIOs".

**Footer Text:** 
Espressif Systems
21 ESP32-C6 Series Datasheet v1.4

**Link at the bottom of page:**
Submit Documentation Feedback