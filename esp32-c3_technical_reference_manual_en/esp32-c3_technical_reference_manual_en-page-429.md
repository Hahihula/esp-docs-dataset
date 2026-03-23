

```markdown
- Setting the `SYSTEM_RSA_MEM_FORCE_PU` bit to force the RSA memory to work as normal when the chip enters light sleep. This bit has the second highest priority, meaning it overrides the `SYSTEM_RSA_MEM_PD` field.
- Setting the `SYSTEM_RSA_MEM_FORCE_PD` bit to send the RSA memory into retention state. This bit has the highest priority, meaning it sends the RSA memory into retention state regardless of the `SYSTEM_RSA_MEM_FORCE_PU` field.

## 16.3.2 Clock Registers

The following registers are used to set clock sources and frequency. For more information, please refer to Chapter 6 Reset and Clock.

- `SYSTEM_CPU_PER_CONF_REG`
- `SYSTEM_SYSCLK_CONF_REG`
- `SYSTEM_BT_LPCCK_DIV_FRAC_REG`

## 16.3.3 Interrupt Signal Registers

The following registers are used for generating the interrupt signals (software interrupt), which then can be routed to the CPU peripheral interrupts via the interrupt matrix. To be more specific, writing 1 to any of the following registers generates an interrupt signal. Therefore, these registers can be used by software to control interrupts. The following registers correspond to the interrupt source SW_INTR_O/1/2/3. For more information, please refer to Chapter 8 Interrupt Matrix (INTERRUPT).

- `SYSTEM_CPU_INTR_FROM_CPU_O_REG`
- `SYSTEM_CPU_INTR_FROM_CPU_1_REG`
- `SYSTEM_CPU_INTR_FROM_CPU_2_REG`
- `SYSTEM_CPU_INTR_FROM_CPU_3_REG`

## 16.3.4 Low-power Management Registers

The following registers are used for low-power management. For more information, please refer to Chapter 9 Low-power Management.

- `SYSTEM_RTC_FASTMEM_CONFIG_REG`: configures the RTC CRC check.
- `SYSTEM_RTC_FASTMEM_CRC_REG`: configures the CRC check value.

## 16.3.5 Peripheral Clock Gating and Reset Registers

The following registers are used for controlling the clock gating and reset of different peripherals. Details can be seen in Table 16.3-2.

- `SYSTEM_CACHE_CONTROL_REG`
- `SYSTEM_PERIP_CLK_ENO_REG`
- `SYSTEM_PERIP_RST_ENO_REG`
```