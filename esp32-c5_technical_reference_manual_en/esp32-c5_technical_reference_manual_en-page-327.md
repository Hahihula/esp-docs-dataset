

```markdown
## 8.17 Interrupts

ESP32-C5's HP IO MUX and HP GPIO matrix can generate the following interrupt signals that will be sent to the Interrupt Matrix.

*   GPIO_EXT_REG_INT
*   GPIO_PROCPU_INT

Several internal interrupt sources from HP IO MUX and HP GPIO matrix can generate the above interrupt signals. The interrupt sources from HP IO MUX and HP GPIO matrix are listed with their trigger conditions and the resulted interrupt signals in Table 8.17-1.

Table 8.17-1. HP IO MUX and HP GPIO Matrix's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
| :------------------------ | :--------------------------------------------- | :--------------- |
| GPIO_EXT_COMP_O_ALL_INT   | See Chapter 47 Analog Voltage Comparator      | GPIO_EXT_REG_INT |
| GPIO_EXT_COMP_O_NEG_INT   | See Chapter 47 Analog Voltage Comparator      | GPIO_EXT_REG_INT |
| GPIO_EXT_COMP_O_POS_INT   | See Chapter 47 Analog Voltage Comparator      | GPIO_EXT_REG_INT |
| GPIO_REG_INTR             | GPIO_STATUS_INTERRUPT[n] & GPIO_PINn_INT_ENA[0] (n: 0~12,23~28) | GPIO_PROCPU_INT |

ESP32-C5's LP IO MUX and GPIO matrix can generate the following interrupt signal that will be sent to the LP_CORE.

*   LP_GPIO_INTR

The interrupt source from LP IO MUX and LP GPIO matrix is listed with its trigger condition and the resulted interrupt signal in Table 8.17-2.

Table 8.17-2. LP IO MUX and LP GPIO Matrix's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
| :------------------------ | :--------------------------------------------- | :--------------- |
| LP_GPIO_REG_INTR          | LP_GPIO_STATUS_INTERRUPT[n] (n: 0~6)           | LP_GPIO_INTR     |

## 8.18 Register Summary

### 8.18.1 HP GPIO Matrix Register Summary

The addresses in this section are relative to HP GPIO matrix base address provided in Table 6.3-2 in Chapter 6 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                     | Description       | Address | Access |
|--------------------------|:------------------|:--------|:-------|
| Configuration Registers  |                  |         |        |
```