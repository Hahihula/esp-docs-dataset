

```markdown
| Internal Interrupt Source | Trigger Condition                                                                 | Interrupt Signal         |
|----------------------------|------------------------------------------------------------------------------------|--------------------------|
| GPIO_COMPn_ALL_INT (n = 0 ~ 1) | Any COMP_OUT signal transition occurs                                             | GPIO_PAD_COMP_INT       |
| GPIO_COMPn_NEG_INT (n = 0 ~ 1) | The COMP_OUT signal changes from high level to low level                          | GPIO_PAD_COMP_INT       |
| GPIO_COMPn_POS_INT (n = 0 ~ 1) | The COMP_OUT signal changes from low level to high level                         | GPIO_PAD_COMP_INT       |

Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4.
```

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 9.19.1 HP GPIO Matrix Register Summary.

## 63.7 Programming Procedures

The programming procedure for the analog voltage comparator is as follows:

Note:
For more information about the register fields mentioned in this section, refer to Chapter 20 System Registers (SYSREG).

1. Enable the comparator by setting LPSYSREG_XPD_COMPn (n = 0 ~ 1) to 1.
2. Disable normal digital pad functions (including IE, OE, WPU, and WPD) for PAD1, and if using the external reference voltage, also for PADO. For detailed configuration, see Chapter 9 GPIO Matrix and IO MUX.
3. Configure the comparison mode by setting LPSYSREG_MODE_COMPn (n = 0 ~ 1):
   - 0: Configures to compare the main voltage with the internal reference voltage;
   - 1: Configures to compare the main voltage with the external reference voltage.
4. Configure the internal reference voltage through LPSYSREG_DREF_COMPn (n = 0 ~ 1), which offers a voltage range of 0 ~ (0.7 × VDD_IO_6) V with a step of 0.1 × VDD_IO_6 V.
```