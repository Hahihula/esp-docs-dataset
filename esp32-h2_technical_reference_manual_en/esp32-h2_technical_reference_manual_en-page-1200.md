

```markdown
Chapter 38 Parallel IO Controller (PARL_IO)

GoBack

## 38.4 Architectural Overview

Clock Domains

- TX Core
- RX Core
- APB
- AHB

Register Group

PARLIO

GDMA_push_inf
TX FIFO
RX FIFO
RX FIFO_inf
TX FIFO_inf
RX FIFO Control
TX FIFO Control

GDMA_pop_inf

Clock Generator

XTAL_CLK
PLL_F96M_CLK
RC_FASK_CLK

PAD_CLK_RX
PAD_CLK_TX
CLK_TX_out
CLK_RX_out

CLK_RX
CLK_TX

IO Bus

RXD
TXD

Figure 38.4-1. PARLIO Architecture

Figure 38.4-1 shows the architecture of PARLIO. In addition to the RX unit and the TX unit, a group of status configuration registers is also included.

The RX unit converts RXD into an asynchronous FIFO interface, which synchronizes RXD to the AHB clock domain. RXD is then converted to a standard GDMA interface and sent to the internal memory.

The TX unit fetches data from internal memory through GDMA and converts the GDMA interface into an asynchronous FIFO interface. The asynchronous FIFO synchronizes the data to the TX Core clock domain and converts the data to TXD for parallel IO bus output.

## 38.5 Functional Description

### 38.5.1 Clock Generator

There are four input clock domains in PARLIO, namely, RX Core, TX Core, AHB, and APB, as shown in Figure 38.4-1.

The status configuration register group works in the APB clock domain.

The GDMA interface logic works in the AHB clock domain.

RX Core and TX Core clock domains each have four clock sources for selection, i.e., the internal system clock sources XTAL_CLK, RC_FAST_CLK, PLL_F96M_CLK and the external clock source (PAD_CLK_TX/RX), as
```