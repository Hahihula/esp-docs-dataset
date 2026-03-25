

```markdown
## 35.12 I2S Interrupts

ESP32-C5's I2S can generate the `I2S_INTR` interrupt signal that will be sent to the **Interrupt Matrix**. There are several internal interrupt sources from I2S that can generate the above interrupt signal(s) as follows:

*   `I2S_TX_HUNG_INT`: Triggered when data transmission is timed out. For example, if the I2S module is configured as TX slave mode, but the master does not provide BCK or WS signals for a long time (specified in `I2S_LC_HUNG_CONF_REG`), this interrupt will be triggered.
*   `I2S_RX_HUNG_INT`: Triggered when the data reception is timed out. For example, if the I2S module is configured as RX slave mode, but the master does not transmit data for a long time (specified in `I2S_LC_HUNG_CONF_REG`), this interrupt will be triggered.
*   `I2S_TX_DONE_INT`: Triggered when sending data is complete, i.e., all data in I2S TX FIFO has been sent.
*   `I2S_RX_DONE_INT`: Can be triggered in different ways depending on the configured value of `I2S_RX_DONE_MODE`:
    - 0: Triggered when the number of bytes received by I2S RX is greater than the receive length value configured by `I2S_RX_EOF_NUM_REG`;
    - 1: Triggered when the GDMA RX FIFO is full.

**Note:**  
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 11 **Interrupt Matrix > Section 11.2 Terminology**.

Each interrupt source can be configured by a common set of registers that are described in Section *Interrupt Configuration Registers*. The specific registers can be found in Section *35.14 Register Summary*.


## 35.13 Software Configuration Process

### 35.13.1 Configure I2S as TX Mode

Follow the steps below to configure I2S as TX mode via software:

1.  Configure the clock as described in Section *35.6*.
2.  Configure signal pins according to Table *35.4-1*.
3.  Select the mode needed by configuring `I2S_TX_SLAVE_MOD`.
    *   0: Master TX mode
    *   1: Slave TX mode
4.  Set needed TX data mode and TX channel mode as described in Section *35.9*, and then set `I2S_TX_UPDATE`.
5.  Reset TX unit and TX FIFO as described in Section *35.7*.
6.  Enable corresponding interrupts. See Section *35.12*.
7.  Configure GDMA outlink.
```