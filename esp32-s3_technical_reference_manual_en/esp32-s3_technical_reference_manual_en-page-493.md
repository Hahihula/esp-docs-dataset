Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

Subtitle: GoBack

Section Title: 6.12 IO MUX Function List

Body Text:
Table 6.12-1 shows the IO MUX functions of each GPIO pin.

Subsection Titles with Table Headers:

- GPIO
- Pin Name
- Function O
- Function 1
- Function 2
- Function 3
- Function 4
- DRV
- RST
- Notes

Table Content:
- Row: 0, GPIO0, GPIO0, GPIOO0, -, 2, 3, R
- Row: 1, GPIO1, GPIO1, GPIOI1, -, 2, 1, R
- Row: 2, GPIO2, GPIO2, GPIO2, -, 2, 1, R
- Row: 3, GPIO3, GPIO3, GPIO3, -, 2, 1, R
- Row: 4, GPIO4, GPIO4, GPIO4, -, 2, O, R
- Row: 5, GPIO5, GPIO5, GPIO5, -, 2, O, R
- Row: 6, GPIO6, GPIO6, GPIO6, -, 2, O, R
- Row: 7, GPIO7, GPIO7, GPIO7, -, 2, O, R
- Row: 8, GPIO8, GPIO8, GPIO8, SUBSPSICS1, - , 2, O, R
- Row: 9, GPIO9, GPIO9, GPIO9, SUBSPIPHD, FSPIHD, 2, I, R
- Row: 10, GPIO10, GPIO10, GPIO10, SUBSPCSIC, FSPICSOSO, - , 2, O, R
- Row: 11, GPIO11, GPIO11, GPIO11, SUBSPID, FSPIOD, 2, I, R
- Row: 12, GPIO12, GPIO12, GPIO12, FSPSIO6, - , 2, O, R
- Row: 13, GPIO13, GPIO13, GPIO13, SUBSPIQ, FSPIQ, 2, I, R
- Row: 14, GPIO14, GPIO14, GPIO14, FSPIDQS, - , 2, O, R
- Row: 15, XTAL_32K_P, GPIO15, UORTS, -, 2, O, -
- Row: 16, XTAL_32K_N, GPIO16, UOCTS, -, 2, I, R
- Row: 17, GPIO17, GPIO17, GPIO17, U1TXD, - , 2, L, -
- Row: 18, GPIO18, GPIO18, GPIO18, U1RXD, CLK_OUT3, 2, I, R
- Row: 19, GPIO19, GPIO19, GPIO19, U1RTS, - , 2, O, -
- Row: 20, GPIO20, GPIO20, GPIO20, U1CTS, CLK_OUT1, 3, I, R
- Row: 21, GPIO21, GPIO21, GPIO21, -, 2, L, -
- Row: 26, SPICS1, SPICS1, GPIO26, -, - , 2, O, -
- Row: 27, SPIHD, SPIHD, GPIO27, -, 3, I, R
- Row: 28, SPIWP, SPIWP, GPIO28, -, 2, L, -
- Row: 29, SPICS0, SPICS0, GPIO29, -, - , 2, O, -
- Row: 30, SPICLK, SPICLK, GPIO30, -, 2, I, R
- Row: 31, SPIQ, SPIQ, GPIO31, -, 2, L, -
- Row: 32, SPID, SPID, GPIO32, -, - , 2, O, -
- Row: 33, GPIO33, GPIO33, GPIO33, SUBSPIHD, SPIIO4, 2, I, R
- Row: 34, GPIO34, GPIO34, GPIO34, FSPICSO, - , 2, O, -
- Row: 35, GPIO35, GPIO35, GPIO35, SUBSPIPHD, SPIIO5, 2, I, R
- Row: 36, GPIO36, GPIO36, GPIO36, FSPIDCLK, - , 2, O, -
- Row: 37, GPIO37, GPIO37, GPIO37, SUBSPIQ, SPIIO6, 2, I, R
- Row: 38, GPIO38, GPIO38, GPIO38, FSPIDWP, - , 2, L, -
- Row: 39, MTCK, MTCK, GPIO39, CLK_OUT3, SUBSPIPHD, 1*, -
- Row: 40, MTDO, MTDO, GPIO40, CLK_OUT2, -, 2, I, R
- Row: 41, MTDI, MTDI, GPIO41, CLK_OUT1, -, - , -

Footer:
Espressif Systems

Page Number and Document Version Information:

493 ESP32-S3 TRM (Version 1.7)

Button Texts at the Bottom of Page:
- Submit Documentation Feedback