Title: Chapter 39 On-Chip Sensors and Analog Signal Processing

Subtitle: For specific DMA configuration, please refer to Chapter 3 GDMA Controller (GDMA).

Section Title: DIG ADC FSM

Subsection Numbered Title: **39.3.7.3 DIG ADC FSM**

Body Text:
DIG ADC FSM1 drive SAR ADC1 to sample voltage in cycles according to the order and channel No. specified in the pattern table.

- DIG ADC FSM1 receive the sampling enable signal from the timer.
- Then initiate a sampling request to SAR ADC1 according to the channel and attenuation configuration specified in the current pattern table entry pointed by the pointer (PR).
- Update the PR once the sampling is done.
  - If the PR reaches to the entry length configured in APB_SARADC_SAR1_PATT_LEN, then the PR is reset, and restarts from the first entry of the pattern table.
  - Otherwise, the PR goes to the next entry.

Subsection Numbered Title: **39.3.7.4 Pattern Table**

Body Text:
DIG ADC FSM1 contain a separate pattern table configured by APB_SARADC_SAR1_PATT_TABx_REG, where x represents the register No. (1 ~ 4) of the pattern table, as shown below:

Table Description: 
- Figure 39.3-4 shows an example with entries labeled cmd0 to cmd7.
- Figure 39.3-5 illustrates entries labeled cmd8 to cmd15.

Additional Information:
cmd n (n = 0 - 3) represents pattern table entries 0 ~ 3 in APB_SARADC_SAR1_PATT_TAB1_REG and Pattern Table Entry 0 - Entry 3.
cmd n (n = 4 - 7) represents pattern table entries 4 ~ 7, as shown for Figure 39.3-5.

cmd n (n = 8 - 11) represents pattern table entries 8 ~ 11 in APB_SARADC_SAR1_PATT_TAB3_REG and Pattern Table Entry 8 - Entry 11.
Figure Caption: "Figure 39.3-6."

Footer:
Espressif Systems
Page Number: 1471
Document Title: ESP32-S3 TRM (Version 1.7)
Feedback Link Text: Submit Documentation Feedback

Navigation Link at the top right corner labeled as GoBack.

(Note: The text is transcribed from a technical document, and some parts are described based on their visual representation in images of tables.)