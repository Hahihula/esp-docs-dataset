

```markdown
Chapter 43 Parallel IO Controller (PARLIO)    GoBack


## 43.4 Architectural Overview

Clock Domains

- AXI
- APB
- RX Core
- TX Core

Figure 43.4-1 shows the architecture of PARLIO. In addition to the RX unit and the TX unit, a group of status configuration registers is also included.

The RX unit receives the RXD, stores it in an asynchronous FIFO after the serial-to-parallel conversion, and then stores the data to internal memory via GDMA.

The TX unit fetches data from the internal memory via GDMA, stores it in an asynchronous FIFO, and outputs the data from the IO bus via the TXD signal after the parallel-to-serial conversion.


## 43.5 Functional Description

### 43.5.1 Clock Generator

There are four input clock domains in PARLIO, namely, RX Core, TX Core, AHB, and APB, as shown in Figure 43.4-1.

The status configuration register group works in the APB clock domain.

The GDMA interface logic works in the AHB clock domain.

RX Core and TX Core clock domains each have four clock sources for selection, i.e., the internal system clock sources XTAL_CLK, RC_FAST_CLK, PLL_F240M_CLK, and the external clock source (PAD_CLK_TX/RX), as shown in Figure 43.5-1. Clock sources can be selected by configuring PCR_PARL_CLK_RX_SEL and
```