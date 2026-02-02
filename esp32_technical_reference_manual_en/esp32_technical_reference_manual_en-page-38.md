**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Table Header:**
Table 1.4-4. Input Signals Measured Using the ADC Instruction

| Pad Name/Signal/GPIO | Sar_Mux | Processed by /Sel |
|-----------------------|---------|--------------------|
| SENSOR_VP (GPIO36)    |         |                   |
| SENSOR_CAPP (GPIO37)  |         |                   |
| SENSOR_CAPN (GPIO38)  |         |                   |
| SENSOR_VN (GPIO39)    |         | SAR ADC1/SeI = 0 |
| 32K_XP (GPIO33)       | 5       |                   |
| 32K_XN (GPIO32)       | 6       |                   |
| VDET_1 (GPIO34)      | 7       |                   |
| VDET_2 (GPIO35)      | 8       |                   |
| GPIO4                |         |                   |
| GPIO0                |         |                   |
| GPIO2                |         |                   |
| MTDQ (GPIO15)        |         |                   |
| MTCK (GPIO13)        |         |                   |
| MTDI (GPIO12)        | 6       | SAR ADC2/SeI = 1 |
| MTMS (GPIO14)        | 7       |                   |
| GPIO27               |         |                   |
| GPIO25               |         |                   |
| GPIO26               | 9       |                   |

**Description:**
The instruction prompts the taking of measurements with the use of ADC. Pads/signals available for ADC measurement are provided in Table 1.4-4.

**Subsection Title and Description:**
1.4.12 I2C_RD/I2C_WR – Read/Write I2C

| Sub-address | Data   | Low    | High     |
|-------------|--------|--------|----------|
| 31         |        |        |          |
| 28         |        |        |          |
| 27         |        |        |          |
| 25         |        |        |          |
| 22         |        |        |          |
| 21         |        |        |          |
| 19         |        |        |          |
| 18         |        |        |          |
| 16         |        |        |          |
| 15         |        |        |          |
| 8           |        |        |          |
| 7           |        |        |          |
| 0           |        |        |          |

**Figure Description:**
Figure 1.4-15. Instruction Type – I2C

**Operand and Description Table for Figure Reference (continued):**

| Operand       | Description                                                                                   |
|---------------|---------------------------------------------------------------------------------------------|
| Sub-address   | Slave register address                                                                        |
| Data          | Data to write in I2C_WR operation (not used in I2C_RD operation)                              |
| Low           | High part of bit mask                                                                         |
| High          | Low part of bit mask                                                                          |
| I2C Sel       | Select register n of SENS_I2C_SLAVE_ADDRn (n: 0-7), which contains the I2C slave address.   |
| R/W           | I2C communication direction:                                                                 |
|               | 1 - I2C write                                                                                 |
|               | 0 - I2C read                                                                                    |

**Description for I2C Communication:**
Communicate (read/write) with external I2C slave devices. Details on using the RTC I2C peripheral are provided in section 1.6.

**Note at Bottom of Page:**
Espressif Systems

**Footer Information:**
ESP32 TRM (Version 5.6)

**Link for Feedback Submission:**
Submit Documentation Feedback