**Chapter Title:**
Chapter 8 Interrupt Matrix (INTERRUPT)

**Section Header:**
8.3.2 CPU Interrupt

**Body Text:**
Both of the two CPUs (PRO and APP) have 32 interrupts each, of which 26 are peripheral interrupts. All interrupts in a CPU are listed in Table 8.3-2.

**Table Title:**
Table 8.3-2. CPU Interrupts

| No. | Category      | Type                | Priority Level |
|-----|---------------|---------------------|----------------|
| 0   | Peripheral    | Level-Triggered    | 1              |
| 1   | Peripheral    | Level-Triggered    | 1              |
| 2   | Peripheral    | Level-Triggered    | 1              |
| 3   | Peripheral    | Level-Triggered    | 1              |
| 4   | Peripheral    | Level-Triggered    | 1              |
| 5   | Peripheral    | Level-Triggered    | 1              |
| 6   | Internal      | Timer.0            | 1              |
| 7   | Internal      | Software           | 1              |
| 8   | Peripheral    | Level-Triggered    | 1              |
| 9   | Peripheral    | Level-Triggered    | 1              |
| 10  | Peripheral    | Edge-Triggered     | 1              |
| 11  | Internal      | Profiling          | 3              |
| 12  | Peripheral    | Level-Triggered    | 1              |
| 13  | Peripheral    | Level-Triggered    | 1              |
| 14  | Peripheral    | NMI                | NMI           |
| 15  | Internal      | Timer.1            | 3              |
| 16  | Internal      | Timer.2            | 5              |
| 17  | Peripheral    | Level-Triggered    | 1              |
| 18  | Peripheral    | Level-Triggered    | 1              |
| 19  | Peripheral    | Level-Triggered    | 2              |
| 20  | Peripheral    | Level-Triggered    | 2              |
| 21  | Peripheral    | Level-Triggered    | 3              |
| 22  | Peripheral    | Edge-Triggered     | 3              |
| 23  | Peripheral    | Level-Triggered    | 4              |
| 24  | Peripheral    | Level-Triggered    | 5              |
| 25  | Peripheral    | Level-Triggered    | 4              |
| 26  | Peripheral    | Level-Triggered    | 3              |
| 27  | Peripheral    | Edge-Triggered     | 4              |
| 28  | Peripheral    | Edge-Triggered     | 5              |
| 29  | Internal      | Software           | 3              |
| 30  | Peripheral    | Edge-Triggered     | 4              |
| 31  | Peripheral    | Level-Triggered    | 5              |

**Subsection Header:**
8.3.3 Allocate Peripheral Interrupt Sources to Peripheral Interrupt on CPU

**Body Text (continued):**
In this section:
- Source_X stands for any particular peripheral interrupt source.

**Footer Information:**
Espressif Systems
178 ESP32 TRM (Version 5.6)
Submit Documentation Feedback