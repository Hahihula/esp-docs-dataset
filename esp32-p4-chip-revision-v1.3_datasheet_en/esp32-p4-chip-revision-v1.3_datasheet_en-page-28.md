**Title:**
2 Pins

**Subtitle:**
2.5 Analog Pins

**Table Title:**
Table 2-10. Analog Pins

| Pin No. | Pin Name       | Pin Type | Function                                                                                   |
|---------|---------------|----------|----------------------------------------------------------------------------------------------|
| 78      | FB_DCDC       | —        | Feedback pin of power supply for external DC/DC. It regulates the voltage of VDD_HP_0/2/3 together with feedback resistors of external DC/DC |
| 79      | EN_DCDC       | O        | Enable pin of external DC/DC                                                               |
| 99      | XTAL_N        | —        | External clock input/output connected to chip's crystal or oscillator.                       |
| 100     | XTAL_P        | P/N means differential clock positive/negative.                                             |
| 103     | CHIP_PU       | I        | High: on, enables the chip (powered up). Low: off, disables the chip (powered down).       |

**Note:** 
Do not leave the CHIP_PU pin floating.

---

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

ESP32-P4 Series Datasheet v0.6