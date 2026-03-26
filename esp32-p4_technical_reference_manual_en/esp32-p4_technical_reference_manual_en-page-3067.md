

```markdown
Chapter 63 Analog Voltage Comparator

GoBack

• Voltage comparison mode control

The analog voltage comparator compares the main voltage with the reference voltage, which can either be internal or external. There are two voltage comparison modes depending on the reference voltage selection:

    – Comparing the main voltage with the external reference voltage.
    – Comparing the main voltage with the internal reference voltage.

The voltage comparison mode can be configured through LPSYSREG_MODE_COMPn (n = 0 ~ 1).

• Reference voltage configuration

The internal reference voltage range is 0 ~ (0.7 × VDD_IO_6) V with a step of 0.1 × VDD_IO_6 V, where VDD_IO_6 is the supply voltage of the analog voltage comparator which is equal to the power supply voltage of the chip (usually 3.3 V). The internal reference voltage value can be configured through LPSYSREG_DREF_COMPn (n = 0 ~ 1).

The external reference voltage is accessed directly from the pad with an input range of 0 ~ 0.7 × VDD_IO_6 V, same as the internal reference voltage, requiring no additional configuration.

• Voltage comparison interrupt processing

The voltage comparison result, i.e., the COMP_OUT signal, can be either high or low. Whenever the output value changes, a corresponding interrupt signal is generated.

63.5 Event Task Matrix Feature

The analog voltage comparator on ESP32-P4 supports the Event Task Matrix (ETM) function, which allows analog voltage comparator ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM events related to analog voltage comparator. For more information, please refer to Chapter 13 Event Task Matrix (ETM).

The analog voltage comparator can generate the following ETM events:

• GPIO_EVT_ZERO_DET_POSn: Indicates that the COMP_OUT signal changes from low level to high level, i.e., the main voltage changes from below to above the reference voltage.
• GPIO_EVT_ZERO_DET_NEGn: Indicates that the COMP_OUT signal changes from high level to low level, i.e., the main voltage changes from higher to lower than the reference voltage.

The analog voltage comparator does not support any ETM tasks.

63.6 Interrupts

ESP32-P4’s analog voltage comparator can generate the GPIO_PAD_COMP_INT interrupt signal that will be sent to the Interrupt Matrix.

There are several internal interrupt sources from analog voltage comparator that can generate the above interrupt signal. The interrupt sources from analog voltage comparator are listed with their trigger conditions and the resulted interrupt signal(s) in Table 63.6-1.
```