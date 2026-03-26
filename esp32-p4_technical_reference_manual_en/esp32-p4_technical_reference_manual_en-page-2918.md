

```markdown
Chapter 58 Parallel IO Controller (PARLIO)

The clock can be divided by configuring HP_SYS_CLKRST_PARLIO_RX_CLK_DIV_NUM,  
HP_SYS_CLKRST_PARLIO_RX_CLK_DIV_DENOMINATOR, and  
HP_SYS_CLKRST_PARLIO_RX_CLK_DIV_NUMERATOR. The clock division factor can be configured up to (2⁸ − 1).

The TX Core clock domain has four clock sources for selection, i.e., the internal system clock sources XTAL_CLK, RC_FAST_CLK, PLL_F160M_CLK and the external clock source (PAD_CLK_TX), as shown in Figure 58.5-1. Clock sources can be selected by configuring HP_SYS_CLKRST_PARLIO_TX_CLK_SRC_SEL. The clock can be divided by configuring HP_SYS_CLKRST_PARLIO_TX_CLK_DIV_NUM,  
HP_SYS_CLKRST_PARLIO_TX_CLK_DIV_DENOMINATOR, and  
HP_SYS_CLKRST_PARLIO_TX_CLK_DIV_NUMERATOR. The clock division factor can be configured up to (2⁸ − 1).

The input clock of the TX and RX units can be inverted. The operating clock of the TX and RX units can also be inverted before being output to IO. The TX and RX units also support clock gating of the output clock.

Clock Generator

HP_SYS_CLKRST_PARLIO_RX_CLK_SRC_SEL
XTAL_CLK → 0
RC_FAST_CLK → 1
PLL_F160M_CLK → 2
PAD_CLK_RX → 3

CLK_RX_in → DIV → INV → Gate → RX_INV_O → CLK_RX_out

RX_INV_I, RX_Gate_En

HP_SYS_CLKRST_PARLIO_TX_CLK_SRC_SEL
XTAL_CLK → 0
RC_FAST_CLK → 1
PLL_F160M_CLK → 2
PAD_CLK_TX → 3

CLK_TX_in → DIV → INV → Gate → TX_INV_O → CLK_TX_out

TX_INV_I, TX_Gate_En

Figure 58.5-1. PARLIO Clock Generation

58.5.2 Clock & Reset Restriction

Due to the versatility of PARLIO, the PAD clocks (PAD_CLK_TX/RX) of PARLIO may come from different masters (external devices or internal clock sources). These clocks might be either free-running clock or not. If the clock is not free-running, some internal control signals of PARLIO cannot process CDC, so there are certain restrictions during the operation.

1. During the reset of the asynchronous FIFO, it takes two clock cycles to synchronize within AXI clock domain and Core clock domain. Therefore, if the reset of AXI clock domain is performed with a clock that is not free-running, the reset synchronization must be performed two clock cycles in advance. The specific operation is shown in the table below.
```