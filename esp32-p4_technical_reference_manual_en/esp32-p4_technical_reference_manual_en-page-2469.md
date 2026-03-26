

```markdown
## 46.12 I2S Interrupts

ESP32-P4's `I2Sn` can generate the `I2Sn_INTR` interrupt signal that will be sent to the **Interrupt Matrix**. There are several internal interrupt sources from `I2Sn` that can generate the above interrupt signal(s) as follows:

- `I2Sn_TX_HUNG_INT`: Triggered when data transmission is timed out. For example, if the `I2Sn` module is configured as TX slave mode, but the master does not provide BCK or WS signals for a long time (specified in `I2S_LC_HUNG_CONF_REG`), this interrupt will be triggered.
- `I2Sn_RX_HUNG_INT`: Triggered when the data reception is timed out. For example, if the `I2Sn` module is configured as RX slave mode, but the master does not transmit data for a long time (specified in `I2S_LC_HUNG_CONF_REG`), this interrupt will be triggered.
- `I2Sn_TX_DONE_INT`: Triggered when data transmission is completed.
- `I2Sn_RX_DONE_INT`: Triggered when the data reception is completed.

**Note:**
For definitions of *interrupt*, *interrupt signal*, *interrupt source*, and their correlations, please refer to Chapter 12 **Interrupt Matrix > Section 12.2 Interrupt Terminology in ESP32-P4**.

Each interrupt source can be configured by a common set of registers that are described in Section **Interrupt Configuration Registers**. The specific registers can be found in Section **46.14 Register Summary**.

## 46.13 Software Configuration Process

### 46.13.1 Configure I2S as TX Mode

Follow the steps below to configure `I2Sn` as TX mode via software:

1. Configure the clock as described in Section **46.6**.
2. Configure signal pins according to Table **46.4-1**.
3. Select the mode needed by configuring `I2S_TX_SLAVE_MOD`.
    - 0: Master TX mode
    - 1: Slave TX mode
4. Set needed TX data mode and TX channel mode as described in Section **46.9**, and then set `I2S_TX_UPDATE`.
5. Reset TX unit and TX FIFO as described in Section **46.7**.
6. Enable corresponding interrupts. See Section **46.12**.
7. Configure GDMA outlink.
8. Set `I2S_TX_STOP_EN` if needed. For more information, please refer to Section **46.8.1**.
9. Start transmitting data:
    - In master mode, wait till `I2Sn` slave gets ready, then set `I2S_TX_START` to start transmitting data;
```