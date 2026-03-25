

```markdown
| GPIO_REG_INTR | GPIO_STATUS_INTERRUPT[n] & GPIO_PINn_INT_ENA[0] (n: 0~13, 22~29) | GPIO_PROCPU_INT |
|---------------|-------------------------------------------------------------|-----------------|
```

ESP32-C61's LP IO MUX and LP GPIO matrix can generate the following interrupt signal that will be sent to the LP_CORE.

*   LP_GPIO_INTR

The interrupt source from LP IO MUX and LP GPIO matrix is listed with its trigger condition and the resulted interrupt signal in Table 6.17-2.

Table 6.17-2. LP IO MUX and LP GPIO Matrix's Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition | Interrupt Signal |
|---------------------------|-------------------|------------------|
| LP_GPIO_REG_INTR          | LP_GPIO_STATUS_INTERRUPT[n] (n: 0~6) | LP_GPIO_INTR |

## 6.18 Register Summary

### 6.18.1 HP GPIO Matrix Register Summary

The addresses in this section are relative to HP GPIO matrix base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Configuration Registers** | | | |
| GPIO_STRAP_REG | Strapping pin register | 0x0000 | RO |
| GPIO_OUT_REG | GPIO output register | 0x0004 | R/W/SC/WTC |
| GPIO_OUT_W1TS_REG | GPIO output set register | 0x0008 | WT |
| GPIO_OUT_W1TC_REG | GPIO output clear register | 0x000C | WT |
| GPIO_ENABLE_REG | GPIO output enable register | 0x0034 | R/W/WTC |
| GPIO_ENABLE_W1TS_REG | GPIO output enable set register | 0x0038 | WT |
| GPIO_ENABLE_W1TC_REG | GPIO output enable clear register | 0x003C | WT |
| GPIO_IN_REG | GPIO input register | 0x0064 | RO |
| **Interrupt Status Registers** | | | |
| GPIO_STATUS_REG | GPIO interrupt status register | 0x0074 | R/W/WTC |
| GPIO_STATUS_W1TS_REG | GPIO interrupt status set register | 0x0078 | WT |
| GPIO_STATUS_W1TC_REG | GPIO interrupt status clear register | 0x007C | WT |
| GPIO_PROCPU_INT_REG | GPIO_PROCPU_INT interrupt status register | 0x00A4 | RO |
| GPIO_SDIO_INT_REG | GPIO_SDIO_INT interrupt status register | 0x00A8 | RO |
| GPIO_STATUS_NEXT_REG | GPIO interrupt source register | 0x00C4 | RO |
| **Pin Configuration Registers** | | | |
| GPIO_PINO_REG | GPIO0 configuration register | 0x00D4 | R/W |
| GPIO_PIN1_REG | GPIO1 configuration register | 0x00D8 | R/W |
```