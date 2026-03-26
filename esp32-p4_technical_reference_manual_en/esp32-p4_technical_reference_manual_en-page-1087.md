

```markdown
To modify the 16-bit prescaler, please first configure the TIMG_Tx_DIVIDER field, and then set TIMG_Tx_DIVCNT_RST to 1. Meanwhile, the timer must be disabled (i.e., TIMG_Tx_EN should be cleared). Otherwise, the result can be unpredictable.

## 16.3.2 54-bit Time-base Counter

The 54-bit time-base counter is based on TB_CLK and can be configured to increment or decrement via the TIMG_Tx_INCREASE field. The time-base counter can be enabled or disabled by setting or clearing the TIMG_Tx_EN field, respectively. When enabled, the time-base counter increments or decrements on each cycle of TB_CLK. When disabled, the time-base counter is essentially frozen. Note that the TIMG_Tx_INCREASE field can be changed no matter whether TIMG_Tx_EN is set or not, and this will cause the time-base counter to change direction instantly.

To read the 54-bit value of the time-base counter, the timer value must be latched to two registers before being read by the CPU (due to the CPU being 32-bit). By writing any value to the TIMG_TxUPDATE_REG, the current value of the 54-bit timer starts to be latched into the TIMG_TxLO_REG and TIMG_TxHI_REG registers containing the lower 32-bits and higher 22-bits, respectively. When TIMG_TxUPDATE_REG is cleared by hardware, it indicates the latch operation has been completed and current timer value can be read from the TIMG_TxLO_REG and TIMG_TxHI_REG registers. TIMG_TxLO_REG and TIMG_TxHI_REG registers will remain unchanged for the CPU to read in its own time until TIMG_TxUPDATE_REG is written to again.

## 16.3.3 Alarm Generation

A timer can be configured to trigger an alarm when the timer’s current value matches the alarm value. An alarm will cause an interrupt to occur and (optionally) an automatic reload of the timer’s current value (see Section 16.3.4).

The 54-bit alarm value is configured using TIMG_TxALARMLO_REG and TIMG_TxALARMHI_REG, which represent the lower 32-bits and higher 22-bits of the alarm value, respectively. However, the configured alarm value is ineffective until the alarm is enabled by setting the TIMG_Tx_ALARM_EN field. To avoid alarm being enabled “too late” (i.e., the timer value has already passed the alarm value when the alarm is enabled), the hardware will trigger the alarm immediately if the current timer value is:

* higher than the alarm value (within a defined range) when the up-down counter increments
* lower than the alarm value (within a defined range) when the up-down counter decrements

Table 16.3-1 and Table 16.3-2 show the relationship between the current value of the timer, the alarm value, and when an alarm is triggered. The current time value and the alarm value are defined as follows:

* TIMG_VALUE = {TIMG_TxHI_REG, TIMG_TxLO_REG}
* ALARM_VALUE = {TIMG_TxALARMHI_REG, TIMG_TxALARMLO_REG}
```