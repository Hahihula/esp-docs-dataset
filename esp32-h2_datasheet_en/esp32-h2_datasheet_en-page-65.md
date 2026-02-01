Title: Appendix A – ESP32-H2 Consolidated Pin Overview

Table:
- Column headers are as follows (from left to right): 
  - Pin No.
  - Pin Name
  - Pin Type
  - Pin Providing Power At Reset/After Reset
  - Analog Function After Reset = {0, 1}
  - IO MUX Function Type {1, 2, 3} for each of the four types (I/O/T, I/O/P, FSPICQ, etc.)

- Rows contain information about specific pins:
  - Pin No. ranges from 1 to 34.
  - Pin Name includes various pin names like VDD3P3, GPIO0, MTMS, etc.
  - Pin Type is mostly IO or Analog.
  - Pin Providing Power At Reset/After Reset indicates whether the power state changes at reset or after a certain condition (e.g., IE for Input Enable).
  - Analog Function After Reset specifies functions like ADC1_CH0, ADC1_CH1, etc. with values {0, 1}.
  - IO MUX Function Type includes various combinations of I/O/T, I/O/P, FSPICQ, and others.

- Some cells are highlighted in yellow indicating special notes or conditions (e.g., "MTMS" is marked as "I1").

Footer note:
"* For details, see Section 2 Pins. Regarding *highlighted* cells, see Section 2.3.3 Restrictions for GPIOs."

The table provides a detailed overview of the pin functions and configurations specific to ESP32-H2 microcontroller pins.

(Note: Specific cell contents are not transcribed in full due to length constraints.)