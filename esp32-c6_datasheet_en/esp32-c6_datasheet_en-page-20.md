**Title:**
Table 2-4. QFN40 IO MUX Pin Functions

**Table Headers:**
1. **Pin No.:** GPIO, GPIO0 to GPIO30 and GPIO27 to GPIO36.
2. **IO MUX / F0 Name:** GPIO names (e.g., GPIO00, GPIO1).
3. **IO MUX Function 1, 2, 3 Type:** I/O/T or O/T for different functions like SPIQ, SPIPD, etc.

**Table Content:**
- The table lists the pin numbers and their corresponding IO MUX function types.
- Some cells are highlighted in yellow (e.g., GPIO4, GPIO5) indicating specific functionalities such as "MTMS" under F0 Name column with type I/O/T for GPIO4. 

**Footnotes:**
1. Bold marks the default pin functions in the default boot mode; see Section 3.1 Chip Boot Mode Control.
2. Regarding highlighted cells (e.g., GPIO5, GPIO8), refer to Section 2.3.4 Restrictions for GPIOs and LP GPIOs.

**Additional Information at Bottom:**
- Each IO MUX function is associated with a type as follows:
   - I – input
   - O – output
   - T – high impedance

- If the pin assigned has functions other than Fn, the input signal of Fn (highlighted in red) or F0 (highlighted in yellow), it's always 1.
- IO is an input; if a pin function as a function other than Fn and F0 are highlighted.

**Footer:**
Espressif Systems
20 ESP32-C6 Series Datasheet v1.4

**Note:** The image also contains some text at the bottom which seems to be part of submission documentation feedback, but it is not fully visible or clear in this context provided by the table and its headers.