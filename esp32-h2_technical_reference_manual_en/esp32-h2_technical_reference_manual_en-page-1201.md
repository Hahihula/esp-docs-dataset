

```markdown
Figure 38.5-1. PARLIO Clock Generation

38.5.2    Clock & Reset Restriction

Due to the versatility of PARLIO, the PAD clocks (PAD_CLK_TX/RX) of PARLIO may come from different masters (external devices or internal clock sources). These clocks might be either free-running clock or not. If the clock is not free-running, some internal control signals of PARLIO cannot process CDC, so there are certain restrictions during the operation.

1. During the reset of the asynchronous FIFO, it takes two clock cycles to synchronize within AHB clock domain and Core clock domain. Therefore, if the reset of AHB clock domain is performed with a clock that is not free-running, the reset synchronization must be performed two clock cycles in advance. The specific operation is shown in the table below.

Table 38.5-1. Operations to Reset AHB Clock Domain with Clock Restrictions

| The Current Frame | Clock Restriction | Specific Operation |
|:------------------|:------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                  | The Next Frame    |                                                                                                                        |
| Free-running clock | Not free-running clock | Users can reset the next frame transfer before switching to the clock that is not free-running. After the reset is completed, users can switch the clock. |
| Not free-running clock | Free-running clock   | The next frame can be reset freely. Users only need to ensure that there is an interval of two clock cycles between the reset and the start of the transfer. |
| Not free-running clock | Not free-running clock | If the next frame transfer needs to be reset, users need to first switch to the internal free-running clock, and then switch to the actual clock after the reset is completed. |
```