

```markdown
- Provide two threshold monitors that can trigger an interrupt when the filtered data is above a high threshold or below a low threshold
- Support continuous transfer of conversion results to memory via the GDMA interface

• LP ADCx controllers:
  - Support one-shot sampling mode
  - Support sampling in sleep mode (e.g., Deep-sleep)
• Support for several Event Task Matrix (ETM) related events and tasks


## 62.4 Architecture

The major components of SAR ADCs and their interconnections are shown in Figure 62.4-1.

![Figure 62.4-1. SAR ADC Architecture](image_path_if_available)

- →: clock signals
- [ ]: clock divider, clock mux, and the blocks the clock works for

As Figure 62.4-1 shows, the SAR ADC module contains the following major functional blocks:

• SAR ADC1: Samples analog inputs from up to 8 pins
• SAR ADC2: Samples analog inputs from up to 6 pins
• Clock Management: Selects clock source and division
• Timer: Dedicated timer for the HP ADCx controllers to generate sampling enable signal.
• HP ADC FSMx: FSM1 and FSM2 that can:
```