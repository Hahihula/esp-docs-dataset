

# Chapter 4

## GDMA Controller (GDMA-AHB, GDMA-AXI)

### 4.1 Overview

General Direct Memory Access (GDMA) is a feature that allows peripheral-to-memory, memory-to-peripheral, and memory-to-memory data transfer at high speed. The CPU is not involved in the GDMA transfer and therefore is more efficient with less workload.

ESP32-P4 has two types of general-purpose DMA controllers, namely GDMA-AHB and GDMA-AXI, to directly access the AHB bus or the AXI bus respectively. Both GDMA-AHB and GDMA-AXI have six independent channels, i.e., three transmit channels and three receive channels.

The GDMA-AHB channels are shared and can be assigned to I3C, UHCI, I2S, ADC, or RMT to access internal and external memory.

The GDMA-AXI channels are also shared and can be assigned to LCD, CAM, two general-purpose SPIs, PARLIO, AES, or SHA to access internal and external memory.

GDMA-AHB and GDMA-AXI use configurable priority and weight arbitration schemes to manage peripherals' needs for bandwidth.

Unless otherwise specified, the term "GDMA controller" refers to both GDMA-AHB and GDMA-AXI in the following text.

Figure 4.1-1. Modules that Share GDMA-AHB Channels

```markdown
GDMA-AHB Channels                    Modules
-------------------------------------|-----------------------------
GDMA-AHB Rx channel 0                 I3C
GDMA-AHB Tx channel 0                 UHCI
GDMA-AHB Rx channel 1                 I2S
GDMA-AHB Tx channel 1                 ADC
GDMA-AHB Rx channel 2                 RMT
GDMA-AHB Tx channel 2
```