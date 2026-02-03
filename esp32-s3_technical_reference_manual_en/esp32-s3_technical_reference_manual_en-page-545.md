**Chapter Title:**
Chapter 9 Interrupt Matrix (INTERRUPT)

**Table of Interrupt Sources and Details**

| No. | Category      | Type       | Priority |
|-----|--------------|-----------|----------|
| 11  | Internal     | Profiling | 3        |
| 12  | Peripheral   | Level-triggered | 1    |
| 13  | Peripheral   | Level-triggered | 1    |
| 14  | Peripheral   | NMI       | NMI      |
| 15  | Internal     | Timer.1   | 3        |
| 16  | Internal     | Timer.2   | 5        |
| 17  | Peripheral   | Level-triggered | 1    |
| 18  | Peripheral   | Level-triggered | 1    |
| 19  | Peripheral   | Level-triggered | 2    |
| 20  | Peripheral   | Level-triggered | 2    |
| 21  | Peripheral   | Level-triggered | 3    |
| 22  | Peripheral   | Edge-triggered | 3    |
| 23  | Peripheral   | Level-triggered | 4    |
| 24  | Peripheral   | Level-triggered | 4    |
| 25  | Peripheral   | Level-triggered | 4    |
| 26  | Peripheral   | Level-triggered | 5    |
| 27  | Peripheral   | Level-triggered | 3    |
| 28  | Peripheral   | Edge-triggered | 4    |
| 29  | Internal     | Software  | 3        |
| 30  | Peripheral   | Edge-triggered | 4    |
| 31  | Peripheral   | Level-triggered | 5    |

**Section Title:**
9.3.3 Allocate Peripheral Interrupt Source to CPUx Interrupt

**Body Text:**

In this section, the following terms are used to describe the operation of the interrupt matrix.

- **Source_Y**: stands for a peripheral interrupt source, wherein, Y means the number of this interrupt source in Table 9.3-1.
  
- **INTERRUPT_COREx_SOURCE_Y_MAP_REG**: stands for a configuration register for the peripheral interrupt source (Source_Y) of CPUx.

- **Interrupt_P**: stands for the CPUx peripheral interrupt numbered as Num_P. The value of Num_P can be 0 ~ 5, 8 ~ 10, 12 ~ 14, 17 ~ 28, and 30 ~ 31. See Table 9.3-2.

- **Interrupt_I**: stands for the CPUx internal interrupt numbered as Num_I. The value of Num_I can be 6, 7, 11, 15, 16, and 29. See Table 9.3-2.

**Subsection Title:**
9.3.3.1 Allocate one peripheral interrupt source (Source_Y) to CPUx

**Body Text:**

Setting the corresponding configuration register INTERRUPT_COREx_SOURCE_Y_MAP_REG of Source_Y to Num_P allocates this interrupt source to Interrupt_P. Num_P here can be any value from 0 ~ 5, 8 ~ 10, 12 ~ 14, 17 ~ 28, and 30 ~ 31. Note that one CPUx interrupt can be shared by multiple peripherals.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)