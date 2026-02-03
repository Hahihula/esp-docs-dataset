Title: Chapter 9 Interrupt Matrix (INTERRUPT)

Subtitle: GoBack

Section Title: 9.3.2 CPU Interrupts

Body Text:
Each CPU has 32 interrupts, numbered from 0 ~ 31, including 26 peripheral interrupts and six internal interrupts.

- Peripheral interrupts: triggered by peripheral interrupt sources, include the following types:
  - Level-triggered interrupts: triggered by a high level signal. The interrupt sources should hold the level till the CPUx handles the interrupts.
  - Edge-triggered interrupts: triggered on a rising edge. CPUx responds to this kind of interrupts immediately.

- NMI interrupt: once triggered, the NMI interrupt cannot be masked by software using the CPUx internal registers. World Controller provides a way to mask such kinds of interrupts. For more information, see Chapter 16 World Controller (WCL).

- Internal interrupts: generated inside CPUx, include the following types:
  - Timer interrupts: triggered by internal timers and are used to generate periodic interrupts.
  - Software interrupts: triggered when software writes to special registers.
  - Profiling interrupt: triggered for performance monitoring and analysis.

Level-triggered and edge-triggered both describe the ways of CPUx to accept interrupt signals. For level-triggered interrupts, the level of interrupt signal should be kept till the CPU handles the interrupt; otherwise the interrupt may be lost. For trigger-edged interrupts, when a rising edge is detected, this edge will be recorded by CPUx, which then allows the interrupt signal to be released.

Interrupt matrix routes the peripheral general interrupt sources to any of the CPUx peripheral interrupts. By such way, CPUx can receive the interrupt signals from peripheral interrupt sources. Table 9.3-2 lists all the interrupts and their types as well as priorities.
ESP32-S3 supports the above-mentioned 32 interrupts at six levels as shown in the table below. A higher level corresponds to a higher priority. NMI has the highest interrupt priority and once triggered, the CPUx must handle such an interrupt. Nested interrupts are also supported, i.e., low-level interrupts can be stopped by high-level interrupts.

Table Title: Table 9.3-2. CPU Interrupts

Table:
| No. | Category     | Type            | Priority |
|-----|--------------|-----------------|----------|
| 0   | Peripheral   | Level-triggered | 1        |
| 1   | Peripheral   | Level-triggered | 1        |
| 2   | Peripheral   | Level-triggered | 1        |
| 3   | Peripheral   | Level-triggered | 1        |
| 4   | Peripheral   | Level-triggered | 1        |
| 5   | Peripheral   | Level-triggered | 1        |
| 6   | Internal     | Timer.0         | 1        |
| 7   | Internal     | Software       | 1        |
| 8   | Peripheral   | Level-triggered | 1        |
| 9   | Peripheral   | Level-triggered | 1        |
| 10  | Peripheral   | Edge-triggered  | 1        |

Footer: Espressif Systems

Page Number and Document Version:
544 ESP32-S3 TRM (Version 1.7)

Link Texts/Buttons:
- Submit Documentation Feedback
- GoBack