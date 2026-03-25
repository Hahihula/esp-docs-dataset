

```markdown
## 38.3.13.3 Traffic Counters

CAN FD can measure CAN frames transmitted/received on the CAN bus. Upon every successfully transmitted CAN frame, TX_COUNTER increments by 1. Upon every successfully received CAN frame, RX_COUNTER increments by 1. TX_COUNTER can be cleared by writing 1 to TWAIFD_TXFCRST. RX_COUNTER can be cleared by writing 1 to TWAIFD_RXFCRST. When CAN FD is in loopback mode and its own transmitted frame is stored in the RX buffer, RX_COUNTER also increments. Traffic counters are optional in CAN FD. Reading TWAIFD_STCNT to learn whether these counters are enabled.

## 38.3.13.4 Debug Register

CAN FD contains a debug register TWAIFD_DEBUG_REG which directly reflects selected fields of the CAN frame currently being transmitted or received.

## 38.4 Interrupts

ESP32-C5's CAN FD can generate the following interrupt signals that will be sent to the Interrupt Matrix.
* IRQ
* IRQ_TIMER

The following interrupt sources can generate the above interrupt signals, depending on where the interrupt source is from:

* TWAIFD_TXBHCI_INT: Triggered when the TX buffer receives a hardware command from CAN Core which changes the TX buffer state to "TX OK", "error" or "aborted".
* TWAIFD_RBNEI_INT: Triggered when the RX buffer is not empty. Clearing this interrupt and not reading out RX buffer via TWAIFD_RX_DATA will re-activate the interrupt.
* TWAIFD_BSI_INT: Triggered when the bit rate shifts.
* TWAIFD_RXFI_INT: Triggered when the RX buffer is full.
* TWAIFD_OFI_INT: Triggered when overload frame transmission is started.
* TWAIFD_BEI_INT: Triggered when error frame transmission is started.
* TWAIFD_ALI_INT: Triggered when arbitration is lost.
* TWAIFD_FCSI_INT: Triggered when the fault confinement state changes. This interrupt is set when the node turns error-passive from error-active, bus-off from error-passive, or error-active from bus-off after reintegration or from error-passive.
* TWAIFD_DOI_INT: Triggered when data overrun occurs. Before this interrupt is cleared, TWAIFD_DOI_INT_ST must be cleared to avoid setting this interrupt again.
* TWAIFD_EWLI_INT: Triggered when the error warning limit (EWL) is reached. When both TX/RX error counters (TEC/REC) reach EWL, this interrupt is generated. When the interrupt is cleared, and REC or TEC is still equal to or higher than EWL, the interrupt will not be generated again.
* TWAIFD_TXI_INT: Triggered when a frame is transmitted.
* TWAIFD_RXI_INT: Triggered when a frame is received.
```