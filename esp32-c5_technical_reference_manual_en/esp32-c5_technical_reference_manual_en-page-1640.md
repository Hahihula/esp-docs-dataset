

```markdown
PCR_PARL_CLK_TX_SEL. The clock can be divided by configuring PCR_PARL_CLK_RX_DIV_NUM and PCR_PARL_CLK_TX_DIV_NUM. The clock division factor can be configured up to (2^16 – 1).

The input clock of the TX and RX units can be inverted. The operating clock of the TX and RX units can also be inverted before being output to IO. The TX and RX units also support clock gating of the output clock.

Figure 43.5-1. PARLIO Clock Generation

Clock Generator
PCR_PARL_CLK_RX_SEL
PLL_F240M_CLK
XTAL_CLK
RC_FAST_CLK
PAD_CLK_RX
DIV → CLK_RX_in → INV → CLK_RX
RX_INV

PCR_PARL_CLK_TX_SEL
PLL_F240M_CLK
XTAL_CLK
RC_FAST_CLK
PAD_CLK_TX
DIV → CLK_TX → INV → CLK_TX_out
TX_INV

43.5.2 Clock and Reset Restriction

Due to the versatility of PARLIO, the PAD clocks of PARLIO (PAD_CLK_TX/RX) may come from different masters (external devices or internal clock sources). These clocks might be either free-running clock or not. If the clock is not free-running, some internal control signals of PARLIO cannot process CDC, so there are certain restrictions during the operation.

1. During the reset of the asynchronous FIFO, it takes two clock cycles to initialize FIFO. Therefore, if the reset of AHB clock domain is performed with a clock that is not free-running, the reset synchronization must be performed two clock cycles in advance. The specific operation is shown in the table below.

Table 43.5-1. Operations to Reset AHB Clock Domain with Clock Restrictions

| Clock Restriction | Specific Operation |
|:------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| The Current Frame | The Next Frame | Users can reset the next frame transfer before switching to the clock that is not free-running. After the reset is completed, users can switch the clock. |
| Free-running clock | Not free-running clock | The next frame can be reset freely. Users only need to ensure that there is an interval of two clock cycles between the reset and the start of the transfer. |
| Not free-running clock | Free-running clock | If the next frame transfer needs to be reset, users need to first switch to the internal free-running clock, and then switch to the actual clock after the reset is completed. |
```