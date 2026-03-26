

```markdown
Register 53.18. TWAI_INTERRUPT_ENABLE_REG (0x0010)

TWAI_EXT_RECEIVE_INT_ENA    Write 1 to enable the TWAI_RX_INT interrupt. (R/W)
TWAI_EXT_TRANSMIT_INT_ENA   Write 1 to enable the TWAI_TX_INT interrupt. (R/W)
TWAI_ERR_WARN_INT_ENA       Write 1 to enable the TWAI_ERR_WARN_INT interrupt. (R/W)
TWAI_EXT_DATA_OVERRUN_INT_ENA    Write 1 to enable the TWAI_OVERRUN_INT interrupt. (R/W)
TWAI_TS_COUNTER_OVFL_INT_ENA     Write 1 to enable the TWAI_TS_COUNTER_OVFL_INT interrupt. (R/W)
TWAI_ERR_PASSIVE_INT_ENA         Write 1 to enable the TWAI_ERR_PASSIVE_INT interrupt. (R/W)
TWAI_ARBITRATION_LOST_INT_ENA    Write 1 to enable the TWAI_ARB_LOST_INT interrupt. (R/W)
TWAI_BUS_ERR_INT_ENA             Write 1 to enable the TWAI_BUS_ERR_INT interrupt. (R/W)
TWAI_IDLE_INT_ENA                Write 1 to enable the TWAI_BUS_STATE_INT interrupt. (RO)

Register 53.19. TWAI_DATA_O_REG (0x0040)

TWAI_DATA_O    In Operation mode, configures the 0th byte information of the data to be transmitted, or reads the 0th byte information of the data received. In Reset mode, configures the 1th byte of the filter code. (R/W)
```