

```markdown
PCR_PARL_CLK_TX_SEL. The clock can be divided by configuring PCR_PARL_CLK_RX_DIV_NUM and PCR_PARL_CLK_TX_DIV_NUM. The clock division factor can be configured up to (2^16 − 1).

The input clock of the RX unit can be inverted. The operating clock of the TX unit can also be inverted before being output to IO.

Figure 38.5-1. PARLIO Clock Generation

38.5.2    Clock & Reset Restriction

Due to the versatility of PARLIO, the PAD clocks of PARLIO may come from different masters (external devices or internal clock sources). These clocks might be either free-running clock or not. If the clock is not free-running, some internal control signals of PARLIO cannot process CDC, so there are certain restrictions during the operation.

1. During the reset of the asynchronous FIFO, it takes two clock cycles to synchronize within AHB clock domain and Core clock domain. Therefore, if the reset of AHB clock domain is performed with a clock that is not free-running, the reset synchronization must be performed two clock cycles in advance. The specific operation is as follows:

• Scenario 1: The current frame transfer is based on free-running clock, but the next frame transfer is not based on free-running clock.
    Operation: Users can reset the next frame transfer before switching to the clock that is not free-running. After the reset is completed, users can switch the clock.

• Scenario 2: The current frame transfer is not based on free-running clock, but the next frame transfer is based on free-running clock.
    Operation: The next frame can be reset freely. Users only need to ensure that there is an interval of two clock cycles between the reset and the start of the transfer.

• Scenario 3: Both the current and next frame transfers are not based on free-running clock.
    Operation: If the next frame transfer needs to be reset, users need to first switch to the internal free-running clock, and then switch to the actual clock after the reset is completed.

2. Due to the restrictions caused by a clock that is not free-running, PARL_IO_RX_START and
```