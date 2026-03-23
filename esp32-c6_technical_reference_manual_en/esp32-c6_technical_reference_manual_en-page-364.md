

```markdown
## Register 8.72. PCR_RESET_EVENT_BYPASS_REG (0x0FF0)

PCR_RESET_EVENT_BYPASS_APM Configures to control reset event relationship for tee_reg/apm_reg/hp_system_reg.
- 0: tee_reg/apm_reg/hp_system_reg will not only be reset by power-reset, but also some reset events.
- 1: tee_reg/apm_reg/hp_system_reg will only be reset by power-reset. Some reset events will be bypassed.
(R/W)

PCR_RESET_EVENT_BYPASS Configures to control reset event relationship for system-bus.
- 0: System bus (including arbiter/router) will not only be reset by power-reset, but also some reset events.
- 1: System bus (including arbiter/router) will only be reset by power-reset. Some reset events will be bypassed.
(R/W)

## Register 8.73. PCR_SYSCLK_FREQ_QUERY_O_REG (0x0124)

PCR_FOSC_FREQ Represents the frequency of RC_FAST_CLK.
Measurement unit: MHz
(HRO)

PCR_PLL_FREQ Represents the frequency of PLL_CLK.
Measurement unit: MHz
(HRO)
```