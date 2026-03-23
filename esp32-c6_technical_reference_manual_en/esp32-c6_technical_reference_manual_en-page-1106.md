

```markdown
Register 33.30. TWAI_INT_ST_REG (0x000C)

TWAI_RX_INT_ST The masked interrupt status of TWAI_RX_INT. (RO)
TWAI_TX_INT_ST The masked interrupt status of TWAI_TX_INT. (RO)
TWAI_ERR_WARN_INT_ST The masked interrupt status of TWAI_ERR_WARN_INT. (RO)
TWAI_OVERRUN_INT_ST The masked interrupt status of TWAI_OVERRUN_INT. (RO)
TWAI_ERR_PASSIVE_INT_ST The masked interrupt status of TWAI_ERR_PASSIVE_INT. (RO)
TWAI_ARB_LOST_INT_ST The masked interrupt status of TWAI_ARB_LOST_INT. (RO)
TWAI_BUS_ERR_INT_ST The masked interrupt status of TWAI_BUS_ERR_INT. (RO)
TWAI_BUS_STATE_INT_ST The masked interrupt status of TWAI_BUS_STATE_INT. (RO)

Register 33.31. TWAI_INT_ENA_REG (0x0010)

TWAI_RX_INT_ENA Write 1 to enable the receive interrupt. (R/W)
TWAI_TX_INT_ENA Write 1 to enable the transmit interrupt. (R/W)
TWAI_ERR_WARN_INT_ENA Write 1 to enable the error warning interrupt. (R/W)
TWAI_OVERRUN_INT_ENA Write 1 to enable the data overrun interrupt. (R/W)
TWAI_ERR_PASSIVE_INT_ENA Write 1 to enable the error passive interrupt. (R/W)
TWAI_ARB_LOST_INT_ENA Write 1 to enable the arbitration lost interrupt. (R/W)
TWAI_BUS_ERR_INT_ENA Write 1 to enable the bus error interrupt. (R/W)
TWAI_BUS_STATE_INT_ENA Write 1 to enable the bus state interrupt. (R/W)
```