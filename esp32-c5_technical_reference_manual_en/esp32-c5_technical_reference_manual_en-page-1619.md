

```markdown
Chapter 42 Remote Control Peripheral (RMT)    [GoBack](#)

*   `RMT_CHn_TX_THR_EVENT_INT`: triggered when the amount of data the transmitter has transmitted reaches the value set in `RMT_CHn_TX_LIM_REG`.
*   `RMT_CHm_RX_THR_EVENT_INT`: triggered each time when the amount of data received by the receiver reaches the value set in `RMT_CHm_RX_LIM_REG`.
*   `RMT_CHn_TX_END_INT`: triggered when the transmitter has finished transmitting signals.
*   `RMT_CHm_RX_END_INT`: triggered when the receiver has finished receiving signals.
*   `RMT_CHn_TX_LOOP_INT`: triggered when the loop counting reaches the value set by `RMT_TX_LOOP_NUM_CHn`.

**Note:**
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 11 Interrupt Matrix > Section 11.2 Terminology.

Each interrupt source can be configured by a common set of registers that are described in Section *Interrupt Configuration Registers*. The specific registers can be found in Section 42.6 *Register Summary*.
```