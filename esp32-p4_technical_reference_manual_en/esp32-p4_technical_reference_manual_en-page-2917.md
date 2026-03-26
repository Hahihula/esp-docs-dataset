

```markdown
Chapter 58 Parallel IO Controller (PARLIO)    GoBack


## 58.4 Architectural Overview

Clock Domains

- AXI
- APB
- RX Core
- TX Core

Register Group

GDMA_push_inf
GDMA_pop_inf

RX FIFO
TX FIFO

RX FIFO_inf
TX FIFO_inf

RX FIFO Control
TX FIFO Control

PARLIO

Clock Generator
  - XTAL_CLK
  - PLL_F160M_CLK
  - RC_FASK_CLK

PAD_CLK_RX
PAD_CLK_TX
CLK_TX_out
CLK_RX_out

RXD
TXD

IO Bus

Figure 58.4-1. PARLIO Architecture


Figure 58.4-1 shows the architecture of PARLIO. In addition to the RX unit and the TX unit, a group of status configuration registers is also included.

The RX unit receives the RXD, stores it in an asynchronous FIFO after the serial-to-parallel conversion, and then stores the data to internal memory via GDMA.

The TX unit fetches data from the internal memory via GDMA, stores it in an asynchronous FIFO, and outputs the data from the IO bus via the TXD signal after the parallel-to-serial conversion.


## 58.5 Functional Description

### 58.5.1 Clock Generator

There are four input clock domains in PARLIO, namely, RX Core, TX Core, AXI, and APB, as shown in Figure 58.4-1.

The status configuration register group works in the APB clock domain.

The GDMA interface logic works in the AXI clock domain.

The RX Core clock domain has four clock sources for selection, i.e., the internal system clock source XTAL_CLK, RC_FAST_CLK, PLL_F160M_CLK, and the external clock source (PAD_CLK_RX), as shown in Figure 58.5-1. Clock sources can be selected by configuring HP_SYS_CLKRST_PARLIO_RX_CLK_SRC_SEL.
```