

```markdown
Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 8.18.1 HP GPIO Matrix Register Summary.

## 47.7 Programming Procedures

The programming procedure for the analog voltage comparator is as follows:

**Note:**
For more information about the register fields mentioned in this section, refer to Chapter 8 GPIO Matrix and IO MUX.

1. Set `PCR_IOMUX_FUNC_CLK_EN` to 1.
2. Enable the comparator by setting `GPIO_EXT_XPD_COMP_O` to 1.
3. Disable normal digital pad functions (including IE, OE, WPU, and WPD) for PAD1, and if using the external reference voltage, also for PADO. For detailed configuration, see Chapter 8 GPIO Matrix and IO MUX.
4. Configure the comparison mode by setting `GPIO_EXT_PAD_COMP_CONFIG_O_REG`:
    *   0: Configures to compare the main voltage with the internal reference voltage;
    *   1: Configures to compare the main voltage with the external reference voltage.
5. Configure the internal reference voltage through `GPIO_EXT_DREF_COMP`, which offers a voltage range of 0 ~ (0.7 × VDDPST1) V with a step of 0.1 × VDDPST1 V.
```