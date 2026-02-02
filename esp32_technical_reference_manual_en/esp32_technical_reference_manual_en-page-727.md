**Chapter Title:**
Chapter 30

**Section Heading:**
Remote Control Peripheral (RMT)

**Subsection 1: Introduction**

The RMT (Remote Control) module is primarily designed to send and receive infrared remote control signals that implement on-off keying in a carrier frequency, but due to its design it can be used to generate various types of signals. An RMT transmitter does this by reading consecutive duration values of an active and inactive output from the built-in RAM block, optionally modulating it with a carrier wave. A receiver will inspect its input signal, optionally filtering it, and will place the lengths of time the signal is active and inactive in the RAM block.

The RMT module has eight channels, numbered zero to seven; registers, signals and blocks that are duplicated in each channel are indicated by an `n` which is used as a placeholder for the channel number.

**Subsection 2: Functional Description**

**30.2.1 RMT Architecture**

The RMT module contains eight channels. Each channel has both a transmitter and a receiver, but only one of them can be active in every channel. The eight channels share a 512x32-bit RAM block which can be read and written by the processor cores over the APB bus, read by the transmitters, and written by the receivers. The transmitted signal can optionally be modulated by a carrier wave. Each channel is clocked by a divided-down signal derived from either the APB bus clock or REF_TICK.

**30.2.2 RMT RAM**

The data structure in RAM is shown in Figure 30.2-2. Each 32-bit value contains two 16-bit entries, with two fields in every entry, "level" and "period". "Level" indicates whether a high-/low-level value was received or is going to be sent, while "period" points out the divider-clock cycles for which the level lasts. A zero period is interpreted as an end-marker: the transmitter will stop transmitting once it has read this, and the receiver will write this, once it has detected that the signal it received has gone idle.

Normally, only one block of 64x32-bit worth of data can be sent or received. If the data size is larger than this block size, blocks can be extended or the channel can be configured for the wraparound mode.

The RMT RAM can be accessed via the APB bus. The initial address is `0x3FF56800`. The RAM block is divided into eight 64x32-bit blocks. By default, each channel uses one block (block zero for channel zero, block one for channel one, and so on). Users can extend the memory to a specific channel by configuring the RMT_MEM_SIZE_CHn register; setting this to >1 will prompt the channel to use the memory of subsequent channels.

**Footer:**
Espressif Systems
727

**Navigation Link:** 
GoBack