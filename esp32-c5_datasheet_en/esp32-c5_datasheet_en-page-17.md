**Page Header:**
- Page Number: No.

**Title: Table of Contents**

**Table Title:** 
- Table 2-1 – cont'd from previous page

**Column Headers in the table include:**
- Pin Name (e.g., UOTXD, UORXD)
- Type (e.g., IO, VDDSPI)
- Power Providing
- At Reset
- After Reset
- Pin Function Sets 
    - I/O MUX
    - LP IOMUX
    - Analog

**Table Content:**
1. **Pin 20:** Name = UOTXD; Type = IO; Power Providing = VDDPST1; At Reset = IE, OE; After Reset = I/O MUX.
2. **Pin 21:** Name = UORXD; Type = IO; Power Providing = VDDPST1; At Reset = IE, WPU; After Reset = I/O MUX.
3. **Pin 22:** Name = GPIO13; Type = IO; Power Providing = VDDPST2; At Reset = IE; After Reset = I/O MUX (Analog).
4. **Pin 23:** Name = GPIO14; Type = IO; Power Providing = VDDPST2; At Reset = USB PU, IE, USB PU^4; After Reset = Analog.
5. **Pin 24:** Name = VDDPST2; Type = Power; Pin Function Sets: I/O MUX (Analog).
6. **Pin 25:** Name = SPICS1; Type = IO; Power Providing = VDDSPI; At Reset = WPU, IE, WPU; After Reset = I/O MUX.
7. **Pin 26:** Name = SPIQ0; Type = IO; Power Providing = VDDSPI; At Reset = WPU, IE, WPU; After Reset = I/O MUX (Analog).
8. **Pin 27:** Name = SPIQ; Type = IO; Power Providing = VDDSPI; At Reset = WPU, IE, WPU; After Reset = I/O MUX.
9. **Pin 28:** Name = SPIWP; Type = IO; Power Providing = VDDSPI; At Reset = WPU, IE, WPU; After Reset = Analog.

**Continuation of the table with additional pins:**
- Pin 29 to Pin 40 (partially visible)
- Pin 41 - ANT_2G
- Pin 43 - GND

**Footnotes and Notes in Table:**
1. Bold marks pin function set.
2. In column Power Providing, regarding power supplied by VDD SPI:
   - Power actually comes from the internal rail to VDDSPI.

**Additional Information at Bottom of Page:** 
- ESP32-C5 Technical Reference Manual
- For details on I/O MUX and GPIO Matrix (GPIO, IO MUX).

**Footer:**
- "Espressif Systems"
- Document version information.
- Submit Documentation Feedback.