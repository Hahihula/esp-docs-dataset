**Chapter Title:**
Chapter 35 LED PWM Controller (LEDC)

**Section Titles and Content:**

1. **35.3 Functional Description**
   - Subsection title: "35.3.1 Architecture"
     - Body text:
       - Figure caption for figure number not provided.
       - The four timers can be independently configured, each internally maintains a timebase counter that counts on cycles of reference clock. Each PWM generator will select one timer and uses the timer's counter value as a reference to generate its PWM signal.

   - Subsection title: "35.3.2 Timers"
     - Body text:
       - Figure caption for figure number not provided.
       - Description about each timer in LED PWM Controller internally maintains timebase counter, referencing another diagram (Figure 35.3-1) and explaining the clock signal used by the timebase counter is named ref_pulsex.

   - Subsection title: "35.3.2.1 Clock Source"
     - Body text:
       - LED PWM registers configured software are clocked by APB_CLK.
       - To use the LED PWM peripheral, enable it with APB_CLK signal to LED PWM and set SYSTEM_LEDCC_CLK_EN in SYSTEM_PERIP_CLK_EN_REG register via software setting SYSTEM_LEDCC_RST field in SYSTEM_PERIP_RST_REG. Refer to Table 17-3 for more information.

2. **Additional Information:**
   - Timers choose common clock source from APB_CLK, RC_FAST_CLK and XTAL_CLK (refer Chapter 7 Reset and Clock).
   - Procedure described below:
     - Figure caption not provided.
     - Describes selecting a clock signal via LEDC_CLKx for different signals.

**Footer:**
- Page number: "1311"
- Document version information: ESP32-S3 TRM (Version 1.7)
- Link to submit feedback or documentation issues:
  - Submit Documentation Feedback

**Navigation Links and UI Elements:**
- GoBack link at the top right corner of the page.

(Note: Specific figure numbers are not provided in text, hence they were referenced as "Figure number" where applicable.)