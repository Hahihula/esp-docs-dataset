

```markdown
Chapter 38 Parallel IO Controller (PARL_IO)                                      GoBack


38.4 Architectural Overview

Clock Domains
TX Core
RX Core
APB
AHB

Register Group

GDMA_push_inf
GDMA_pop_inf

PARLIO
TX FIFO
RX FIFO
TX FIFO Control
RX FIFO Control

PAD_CLK_RX
PAD_CLK_TX
CLK_TX_out

XTAL_CLK
PLL_F240M_CLK
RC_FASK_CLK

Clock Generator

IO Bus
RxD
TxD

Figure 38.4-1. PARLIO Architecture


Figure 38.4-1 shows the architecture of PARLIO. In addition to the RX unit and the TX unit, a group of status configuration registers is also included.

The RX unit converts RXD into an asynchronous FIFO interface, which synchronizes RXD to the AHB clock domain. RXD is then converted to a standard GDMA interface and sent to the internal memory.

The TX unit fetches data from internal memory through GDMA and converts the GDMA interface into an asynchronous FIFO interface. The asynchronous FIFO synchronizes the data to the TX Core clock domain and converts the data to TXD for parallel IO bus output.


38.5 Functional Description

38.5.1 Clock Generator

There are four input clock domains in PARLIO, namely, RX Core, TX Core, AHB, and APB.

The status configuration register group works in the APB clock domain.

The GDMA interface logic works in the AHB clock domain.

RX Core and TX Core clock domains each have four clock sources for selection, i.e., the internal system clock sources XTAL_CLK, RC_FAST_CLK, PLL_F240M_CLK, and the external clock source (PAD_CLK_TX/RX), as shown in Figure 38.5-1. Clock sources can be selected by configuring PCR_PARL_CLK_RX_SEL and
```