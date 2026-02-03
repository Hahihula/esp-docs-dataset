**Title:**
Chapter 32 USB On-The-Go (USB)

**Menu:**
GoBack

**Table:**
```
0000h - Core Global CSRs (1 KB)
0400h - Host Mode CSRs (1 KB)
0800h - Device Mode CSRs (1 KB)
OE00h - Power and Clock Gating CSRs (1 KB)
1000h - Device EP0 / Host Channel 0 FIFO (4 KB)
2000h - Device EP1 / Host Channel 1 FIFO (4 KB)
3000h - DFIFO push/pop for Slave mode
Device EPn / Host Channel n FIFO (4 KB) - Reserved

20000h - Direct Access to Data FIFO RAM for Debugging (128 KB)

3FFFFh - DFIFO debug read/write to this region
```

**Figure:**
- **Caption:** Figure 32.3-2. OTG_FS Register Layout

**Subsection Title:**
Power and Clock Gating

**Body Text:**
A single register used to control power-down and gate various clocks.

**Subsection Title:**
32.3.2.2 FIFO Access

**Body Text:**
The OTG_FS makes use of multiple FIFOs to buffer transmitted or received data payloads. The number and type of FIFOs are dependent on Host or Device mode, and the number of channels or endpoints used (see Section 32.3.3). There are two ways to access the FIFOs: DMA mode and Slave mode. When using Slave mode, the CPU will need to access these FIFOs by reading and writing to either the DFIFO push/pop regions or the DFIFO read/write debug region. FIFO access is governed by the following rules:

- Read access to any address in any one of the 4 KB push/pop regions will result in a pop from the shared RX FIFO.
- Write access to a particular 4 KB push/pop region will result in a push to the corresponding endpoint or channel’s TX FIFO given that the endpoint is an IN endpoint, or the channel is an OUT channel.

   - In Device mode, data is pushed to the corresponding IN endpoint's dedicated TX FIFO.
   
   - In Host mode, data is pushed to the non-periodic TX FIFO or the periodic TX FIFO depending on whether the channel is a non-periodic channel, or a periodic channel.

- Access to the 128 KB read/write region will result in direct read/write instead of a push/pop. This is generally used for debugging purposes only.
  
Note that pushing and popping data to and from the FIFOs by the CPU is only required when operating in Slave mode. When operating in DMA mode, the internal DMA will handle all pushing/popping of data to and from the

**Footer:**
Espressif Systems
1230 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback