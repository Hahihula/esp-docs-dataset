

```markdown
2. Due to the restrictions caused by a clock that is not free-running, `PARL_IO_RX_START` and `PARL_IO_TX_START` cannot perform CDC processing. Therefore, it is necessary to wait until `PARL_IO_RX_START` and `PARL_IO_TX_START` are stable before starting the data transfer, otherwise the transfer might enter a metastable state.

Here are the specific operation steps in the RX unit:

(a) Clear `PCR_PARL_CLK_RX_EN` to turn off RX Core clock domain;

(b) Write 1 to `PARL_IO_RX_START`;

(c) Set `PCR_PARL_CLK_RX_EN` to turn on RX Core clock domain;

(d) Operate the external device to start sending data;

(e) Clear `PCR_PARL_CLK_RX_EN` to turn off RX Core clock domain;

(f) Write 0 to `PARL_IO_RX_START`.

Here are the specific operation steps in the TX unit:

(a) Clear `PCR_PARL_CLK_TX_EN` to turn off TX Core clock domain;

(b) Write 1 to `PARL_IO_TX_START`;

(c) Set `PCR_PARL_CLK_TX_EN` to turn on TX Core clock domain;

(d) Operate the external device to start receiving data;

(e) Clear `PCR_PARL_CLK_TX_EN` to turn off TX Core clock domain;

(f) Write 0 to `PARL_IO_TX_START`.

3. Reset should follow the requirements below:

* The clock reset during the chip start-up should follow the sequence below:
    (a) Reset APB clock domain;
    (b) Reset AHB clock domain;
    (c) Reset Core clock domain.
* Inter-frame transfer requires Core clock domain reset and async FIFO reset.

## 43.5.3 Master-Slave Mode

The TX and RX units can function as both master and slave.

When the TX unit serves as master, it is necessary to set the internal free-running clock as the clock source. The TX unit drives TXD on the rising edge of the clock.

When the TX unit functions as a slave device, there are three scenarios, as shown in the table below.
```