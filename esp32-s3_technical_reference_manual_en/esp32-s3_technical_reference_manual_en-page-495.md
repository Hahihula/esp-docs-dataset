Title: Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

Subtitle: GoBack

Section Title:
6.13 RTC IO MUX Pin List

Body Text:
Table 6.13-1 shows the RTC pins, their corresponding GPIO pins and RTC functions.

Subsection Header:
Table 6.13-1. RTC Functions of RTC IO MUX Pins

Table:
| RTC GPIO Num | GPIO Num | Pin Name       | RTC Function |
|--------------|---------|----------------|-------------|
| 0            | GPIO0  | GPIO0          | -           |
| 1            | GPIO1  | GPIO1          | sar_i2c_scl_0^a, sar_i2c_sda_0^a |
| 2            | GPIO2  | GPIO2          | sar_i2c_scl_1^a, sar_i2c_sda_1^a |
| 3            | GPIO3  | GPIO3          | -           |
| 4            | GPIO4  | GPIO4          | -           |
| 5            | GPIO5  | GPIO5          | sar_i2c_scl_0^b, sar_i2c_sda_0^b |
| 6            | GPIO6  | GPIO6          | sar_i2c_scl_1^b, sar_i2c_sda_1^b |
| 7            | GPIO7  | GPIO7          | -           |
| 8            | GPIO8  | GPIO8          | -           |
| 9            | GPIO9  | GPIO9          | -           |
| 10           | GPIO10 | GPIO10         | -           |
| 11           | GPIO11 | GPIO11         | -           |
| 12           | GPIO12 | GPIO12         | -           |
| 13           | GPIO13 | GPIO13         | -           |
| 14           | GPIO14 | GPIO14         | -           |
| 15           | XTAL_32K_P | XTAL_32K_P   | -           |
| 16           | XTAL_32K_N | XTAL_32K_N   | -           |
| 17           | GPIO17 | GPIO17         | -           |
| 18           | GPIO18 | GPIO18         | -           |
| 19           | GPIO19 | GPIO19         | -           |
| 20           | GPIO20 | GPIO20         | -           |
| 21           | GPIO21 | GPIO21         | -           |

Footnote:
^a For more information on the configuration of sar_i2c_xx, see Section RTC I2C Controller in Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V).

Subsection Header:
Table 6.13-2 shows the RTC pins, their corresponding GPIO pins and analog functions.

Table:
| RTC GPIO Num | GPIO Num | Pin Name       | Analog Function |
|--------------|---------|----------------|----------------|
| 0            | 0       | GPIO0          | -              |
| 1            | 1       | GPIO1          | TOUCH1         |
| 2            | 2       | GPIO2          | TOUCH2         |
| 3            | 3       | GPIO3          | TOUCH3         |
| 4            | 4       | GPIO4          | TOUCH4         |
| 5            | 5       | GPIO5          | TOUCH5         |

Subsection Footer:
Espressif Systems
Submit Documentation Feedback

Document Version Information: ESP32-S3 TRM (Version 1.7)