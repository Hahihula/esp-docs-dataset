**Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**Diagram Title (Figure):**
Figure 31.3-2. SAR ADC Outline of Function

**Table Titles:**
- Table 31.3-1 lists all the analog signals that may be sent to the SAR ADC module via the ADC channels.
- Table 31.3-1. Inputs of SAR ADC

**Tables Content:**

**Signal Name | ADC Channel # | Processed by**
|---|---|---|
| VDET_2 | 7 | SAR ADC1 |
| VDET_1 | 6 | - |
| 32K_XN | 5 | - |
| 32K_XP | 4 | - |
| SENSOR_VN | 3 | - |
| SENSOR_CAPN | 2 | - |
| SENSOR_CAPP | 1 | - |
| SENSOR_VP | 0 | - |
| GPIO26 | 9 | SAR ADC2 |
| GPIO25 | 8 | - |
| GPIO27 | 7 | - |
| MTMS | 6 | - |
| MTDI | 5 | - |
| MTCK | 4 | - |
| MTDO | 3 | - |
| GPIO2 | 2 | - |
| GPIO0 | 1 | - |
| GPIO4 | 0 | - |

**Note:**
- Some of the SAR ADC2 pins are used as strapping pins (GPIO0, GPIO2, and GPIO15), thus can not be used freely.

**Footer Information:**
Espressif Systems
742 ESP32 TRM (Version 5.6)
Submit Documentation Feedback