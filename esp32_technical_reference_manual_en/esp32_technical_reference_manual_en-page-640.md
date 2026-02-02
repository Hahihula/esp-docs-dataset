Title: Chapter 28 LED PWM Controller (LEDC)

Subtitles:
- Register 28.7, LEDC_LSCHn_HPOINT_REG (n : 0-7) (0xA4+0x14*n)
- Register 28.8, LEDC_LSCHn_DUTY_REG (n : 0-7) (0xA8+0x14*n)

Body Text:
LED_C_HPOINT_LSCHn: The output value changes to high when Istimerx(x=[0,3]), selected by low-speed channel n, has reached LED_C_HPOINT_LSCHn[19:0]. (R/W)
LED_C_DUTY_LSCHn: The register is used to control output duty. When Istimerx(x=[0,3]), chosen by low-speed channel n, has reached LED_C_LPOIN_T_LSCHn, the output signal changes to low.
(Read/Write)

LEDC_LPOIN_T_LSCHn = (LED_C_HPOINT_LSCHn[19:0] + LEDC_DUTY_LSCHn[24:4]) (1)
LEDC_LPOIN_T_LSCHn = (LED_C_HPOINT_LSCHn[19:0] + LEDC_DUTY_LSCHn[24:4] + 1) (2)

See the Functional Description for more information on when (1) or (2) is chosen.

Footer:
Espressif Systems
640 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

Diagrams/Tables:

- Register 28.7, LEDC_LSCHn_HPOINT_REG Diagram: 
  - Bits are labeled from n to the least significant bit.
  - The diagram shows a binary representation with bits numbered and corresponding values.

- Register 28.8, LEDC_LSCHn_DUTY_REG Diagram:
  - Similar structure as above but includes additional bits for duty control (24:0).
  - Shows how different parts of the register are used to set output levels based on low-speed channel selection.
  
(Note: The exact binary values and bit positions may not be fully visible in this description, so they might need further clarification from a visual inspection.)