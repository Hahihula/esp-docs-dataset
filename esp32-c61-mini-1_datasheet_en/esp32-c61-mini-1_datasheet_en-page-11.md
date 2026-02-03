Title: Pin Definitions

---

**Figure:** ESP32-C61-MINI-1U Pin Layout (Top View)

**Section Title:** 3.2 Pin Description

ESP32-C61-MINI-1 and ESP32-C61-MINI-1U modules each have 53 pins. See pin definitions in Table **3 Pin Description**.

For peripheral pin configurations, please refer to [ESP32-C61 Series Datasheet](#).

---

**Table Title:** Table 3: ESP32-C61-MINI-1 Pin Definitions

| Name | No. | Type^2 | Function |
|------|-----|--------|----------|
| GND  | 1, 2, 11, 14, 36~43, 45~53 | P      | Ground   |
| 3V3  | 3   |        | Power supply |
| NC   | 4, 7, 32~35, 44       | —      | NC       |
| IO2  | 5   | I/O/T  | GPIO2, LP_GPIO2, FSPIQ |
| IO3  | 6   | I/O/T  | MTMS, GPIO3, LP_GPIO3, ADC1_CH1, FSPIHD |
| EN   | 8   | I      | High: on, enables the chip. Low: off, the chip powers off. Note: Do not leave the EN pin floating. |
| IO4  | 9   | I/O/T  | MTDI, GPIO4, LP_GPIO4, ADC1_CH2, FSPIWP |
| IO5  | 10  | I/O/T  | MTCK, GPIO5, LP_GPIO5, ADC1_CH3 |
| IO0  | 12  | I/O/P  | GPIO0, XTAL_32K_P, LP_GPI00 |
| IO1  | 13  | I/O/P  | GPIO1, XTAL_32K_N, LP_GPIO1, ADC1_CHO |
| IO6  | 15  | I/O/T  | MTDIO, GPIO6, LP_GPIO6, FSPICLK |
| IO7  | 16  | I/O/T  | GPIO7, FSPID |

---

**Footer:** Espressif Systems  
Page number: **11**  
Document version note: ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6

[Submit Documentation Feedback](#)