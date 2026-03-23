

```markdown
PARL_IO_TX_START cannot perform CDC processing. Therefore, it is necessary to wait until PARL_IO_RX_START and PARL_IO_TX_START are stable before starting the data transfer, otherwise the transfer might enter a metastable state.

Here are the specific operation steps in the RX unit:

- Clear `PCR_PARL_CLK_RX_EN` to turn off RX Core clock domain;
- Write 1 to `PARL_IO_RX_START`;
- Set `PCR_PARL_CLK_RX_EN` to turn on RX Core clock domain;
- Operate the external device to start sending data;
- Clear `PCR_PARL_CLK_RX_EN` to turn off RX Core clock domain;
- Write 0 to `PARL_IO_RX_START`.

Here are the specific operation steps in the TX unit:

- Clear `PCR_PARL_CLK_TX_EN` to turn off TX Core clock domain;
- Write 1 to `PARL_IO_TX_START`;
- Set `PCR_PARL_CLK_TX_EN` to turn on TX Core clock domain;
- Operate the external device to start receiving data;
- Clear `PCR_PARL_CLK_TX_EN` to turn off TX Core clock domain;
- Write 0 to `PARL_IO_TX_START`.

3. Reset should follow the requirements below:

- The clock reset during the chip start-up should follow the sequence below:
    - First reset APB clock domain;
    - Then reset AHB clock domain;
    - Finally reset Core clock domain.
- Inter-frame transfer requires Core clock domain reset and async FIFO reset.

## 38.5.3 Master-Slave Mode

The TX unit can function as both master and slave while the RX unit can only function as slave.

When the TX unit serves as master, it is necessary to set the internal free-running clock as the clock source. The TX unit drives TXD on the rising edge of the clock.

When the TX unit functions as a slave device, there are three scenarios:

- **Scenario 1:** The clock sent by the master device is a free-running clock.
    *Requirement:* There is no requirement for the acquisition edge of the master clock.

- **Scenario 2:** The clock sent by the master device is not a free-running clock, and the clock waveform is as shown in Figure 38.5-2.
    *Requirement:* The master clock should capture TXD at the falling edge.
```