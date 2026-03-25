

```markdown
- two filters whose filter coefficients are configurable
- two threshold monitors that can trigger an interrupt when the filtered value is below a low threshold or above a high threshold
- continuous transfer of converted data to memory via GDMA interface

• Support for several Event Task Matrix (ETM) related events and tasks


## 40.4 Architecture

The major components of SAR ADC and their interconnections are shown in Figure 40.4-1.

Figure 40.4-1. SAR ADC Architecture

As Figure 40.4-1 shows, the SAR ADC module contains the following major functional blocks:

• Five channels, connected to five pins on the chip
• SAR ADC: analog domain of the SAR ADC module
• DIG ADC Controller: digital domain of the SAR ADC module, mainly including:
    - Clock management module: selects clock source and division
    - DIG ADC FSM: generates the signals required throughout the ADC sampling process
    - Digital_reader: reads data from SAR ADC, driven by DIG ADC FSM

```