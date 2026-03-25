

```markdown
- configurable channel sampling sequence
- two filters whose filter coefficients are configurable
- two threshold monitors that can trigger an interrupt when the filtered value is below a low threshold or above a high threshold
- continuous transfer of converted data to memory via GDMA interface
• Support for several Event Task Matrix (ETM) related events and tasks

## 33.4 Architectural Overview

The major components of SAR ADC and their interconnections are shown in Figure 33.4-1.

![Figure 33.4-1. SAR ADC Architecture](image_path)

As Figure 33.4-1 shows, the SAR ADC module contains the following major functional blocks:

• four channels, connected to four pins on the chip
• SAR ADC: analog domain of the SAR ADC module
• DIG ADC Controller: digital domain of the SAR ADC module, mainly including:
    - Clock management module: selects clock source and division
    - DIG ADC FSM: generates the signals required throughout the ADC sampling process

```markdown