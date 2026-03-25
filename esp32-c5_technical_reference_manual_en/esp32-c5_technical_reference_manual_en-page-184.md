

```markdown
Chapter 5 GDMA Controller (GDMA)

GoBack

Chapter 5

GDMA Controller (GDMA)

5.1 Overview

General Direct Memory Access (GDMA) is a feature that allows peripheral-to-memory, memory-to-peripheral, and memory-to-memory data transfer at high speed. The CPU is not involved in the GDMA transfer and therefore is more efficient with less workload.

GDMA has six independent channels: three transmit channels and three receive channels. The GDMA channels are shared and can be assigned to PARLIO, ADC, UHCI, AES, SHA, I2S or general-purpose SPI (GP-SPI) to access internal or external memory.

GDMA uses configurable priority and weight arbitration schemes to manage peripherals’ needs for bandwidth.

Figure 5.1-1. Modules that Share GDMA Channels

5.2 Features

GDMA has the following features:

• AHB bus architecture
• Programmable length of data to be transferred in bytes
• Access via any address and size
• Alignment:
```