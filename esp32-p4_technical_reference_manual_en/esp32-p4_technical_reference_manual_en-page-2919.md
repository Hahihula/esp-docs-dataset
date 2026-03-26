

```markdown
| Clock Restriction | Specific Operation |
|:-------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| The Current Frame | The Next Frame |
| Free-running clock | Not free-running clock | Users can reset the next frame transfer before switching to the clock that is not free-running. After the reset is completed, users can switch the clock. |
| Not free-running clock | Free-running clock | The next frame can be reset freely. Users only need to ensure that there is an interval of two clock cycles between the reset and the start of the transfer. |
| Not free-running clock | Not free-running clock | If the next frame transfer needs to be reset, users need to first switch to the internal free-running clock, and then switch to the actual clock after the reset is completed. |

2. Due to the restrictions caused by a clock that is not free-running, `PARL_IO_RX_START` and `PARL_IO_TX_START` cannot perform CDC processing. Therefore, it is necessary to wait until `PARL_IO_RX_START` and `PARL_IO_TX_START` are stable before starting the data transfer. Otherwise, the transfer might enter a metastable state.

Here are the specific operation steps for the RX unit:

* Clear `HP_SYS_CLKRST_PARLIO_RX_CLK_EN` to turn off RX Core clock domain;
* Write 1 to `PARL_IO_RX_START`;
* Set `HP_SYS_CLKRST_PARLIO_RX_CLK_EN` to turn on RX Core clock domain;
* Operate the external device to start sending data;
* Clear `HP_SYS_CLKRST_PARLIO_RX_CLK_EN` to turn off RX Core clock domain;
* Write 0 to `PARL_IO_RX_START`.

Here are the specific operation steps for the TX unit:

* Clear `HP_SYS_CLKRST_PARLIO_TX_CLK_EN` to turn off TX Core clock domain;
* Write 1 to `PARL_IO_TX_START`;
* Set `HP_SYS_CLKRST_PARLIO_TX_CLK_EN` to turn on TX Core clock domain;
* Operate the external device to start receiving data;
* Clear `HP_SYS_CLKRST_PARLIO_TX_CLK_EN` to turn off TX Core clock domain;
* Write 0 to `PARL_IO_TX_START`.

3. Reset should follow the requirements below:

* The clock reset during the chip start-up should follow the sequence below:
    * (a) Reset APB clock domain;
    * (b) Reset GDMA clock domain;
    * (c) Reset Core clock domain.
* Inter-frame transfer requires Core clock domain reset and async FIFO reset.
```