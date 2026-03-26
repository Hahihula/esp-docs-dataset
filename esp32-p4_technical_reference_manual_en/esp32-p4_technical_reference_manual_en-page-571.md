

```markdown
| GPIO_INTR0 | GPIO_STATUS_INTERRUPT[n] & GPIO_PINn_INT_ENA[0] (n: 0 ~ 31) | GPIO_INTR0 |
|------------|-------------------------------------------------------------|------------|
| GPIO_INTR0 | GPIO_STATUS1_INTERRUPT[n] & GPIO_PINn+32_INT_ENA[0] (n: 0 ~ 22) | GPIO_INTR0 |
| GPIO_INTR1 | GPIO_STATUS_INTERRUPT[n] & GPIO_PINn_INT_ENA[1] (n: 0 ~ 31) | GPIO_INTR1 |
| GPIO_INTR1 | GPIO_STATUS1_INTERRUPT[n] & GPIO_PINn+32_INT_ENA[1] (n: 0 ~ 22) | GPIO_INTR1 |
| GPIO_INTR2 | GPIO_STATUS_INTERRUPT[n] & GPIO_PINn_INT_ENA[3] (n: 0 ~ 31) | GPIO_INTR2 |
| GPIO_INTR2 | GPIO_STATUS1_INTERRUPT[n] & GPIO_PINn+32_INT_ENA[3] (n: 0 ~ 22) | GPIO_INTR2 |
| GPIO_INTR3 | GPIO_STATUS_INTERRUPT[n] & GPIO_PINn_INT_ENA[4] (n: 0 ~ 31) | GPIO_INTR3 |
| GPIO_INTR3 | GPIO_STATUS1_INTERRUPT[n] & GPIO_PINn+32_INT_ENA[4] (n: 0 ~ 22) | GPIO_INTR3 |

ESP32-P4’s LP IO MUX and GPIO matrix can generate the following interrupt signals that will be sent to the Interrupt Matrix.
• LP_GPIO_INTR0

The interrupt source from LP IO MUX and LP GPIO matrix are listed with their trigger conditions and the resulted interrupt signals in Table 9.18-2.

Table 9.18-2. LP IO MUX and LP GPIO Matrix’s Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
|----------------------------|--------------------|------------------|
| LP_GPIO_INTR               | LP_GPIO_STATUS_DATA[n] (n: 0 ~ 15) | LP_GPIO_INTR |

## 9.19 Register Summary

### 9.19.1 HP GPIO Matrix Register Summary

The addresses in this section are relative to HP GPIO matrix base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| Configuration Registers | | | |
| GPIO_OUT_REG | GPIO0 ~ GPIO31 output register | 0x0004 | R/W/SC/WTC |
| GPIO_OUT_W1TS_REG | GPIO0 ~ GPIO31 output set register | 0x0008 | WT |
| GPIO_OUT_W1TC_REG | GPIO0 ~ GPIO31 output clear register | 0x000C | WT |
| GPIO_OUT1_REG | GPIO32 ~ GPIO56 output register | 0x0010 | R/W/SC/WTC |
| GPIO_OUT1_W1TS_REG | GPIO32 ~ GPIO56 output set register | 0x0014 | WT |
```