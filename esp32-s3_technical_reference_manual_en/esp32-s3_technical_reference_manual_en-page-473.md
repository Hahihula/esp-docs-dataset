Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

Subtitle: 6.3 Architectural Overview

Body Text:
Figure 6.3-1 shows in details how IO MUX, RTC IO MUX, and GPIO matrix route signals from pins to peripherals, and from peripherals to pins.

Caption under diagram:
Figure 6.3-1. Architecture of IO MUX, RTC IO MUX, and GPIO Matrix

Footnotes related to the figure:

1 Only part of peripheral input signals (marked “yes” in column "Direct input through IO MUX" in Table 6.11-1) can bypass GPIO matrix. The other input signals can only be routed to peripherals via GPIO matrix.

2 There are only 45 inputs from GPIO SYNC to GPIO matrix, since ESP32-S3 provides 45 GPIO pins in total.

3 The pins supplied by VDDP3_CPU or by VDDP3_RTC are controlled by the signals: IE, OE, WPU, and WPD.

4 Only part of peripheral outputs (marked “yes” in column "Direct output through IO MUX" in Table 6.11-1) can be routed to pins bypassing GPIO matrix.

5 There are only 45 outputs (GPIO pin X: O ~ 21, 26 ~ 48) from GPIO matrix to IO MUX.

Figure Caption:
Figure 6.3-2 shows the internal structure of a pad, which is an electrical interface between the chip logic and the GPIO pin. The structure is applicable to all 45 GPIO pins and can be controlled using IE, OE, WPU, and WPD signals.

Footer Information: 
Espressif Systems
Page Number: 473
Document Title: ESP32-S3 TRM (Version 1.7)
Feedback Link Text: Submit Documentation Feedback

Diagram Description:
The diagram is a block diagram showing the architecture of IO MUX, RTC IO MUX, and GPIO Matrix with various components labeled such as "Peripheral Signal Y," "GPIO," "RTC GPIO," etc., connected by arrows indicating signal flow.

Note: The text in parentheses within footnotes (e.g., ①) refers to specific sections or tables mentioned elsewhere presumably.