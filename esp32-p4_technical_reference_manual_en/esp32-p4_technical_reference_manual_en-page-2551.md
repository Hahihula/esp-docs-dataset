

```markdown
Software can access these registers whilst in Host or Device modes.

*   **Host Mode CSRs**
    These registers are responsible for the configuration/control/status in Host mode, thus should only be accessed in Host mode. Each channel has its own set of registers within the Host mode CSRs.
*   **Device Mode CSRs**
    These registers are responsible for the configuration/control/status in Device mode, thus should only be accessed in Device mode. Each endpoint has its own set of registers within the Device mode CSRs.
*   **Power and Clock Gating Register**
    A single register controls power-down and gates various clocks.

### 50.4.2.2 FIFO Access

The OTG_FS makes use of multiple FIFOs to buffer the data payloads to be transmitted or to buffer the received data payloads. The number and type of FIFOs are dependent on Host or Device mode, and the number of channels or endpoints used, see Section 50.4.3. There are two ways to access the FIFOs: DMA mode and Slave mode. In Slave mode, the CPU accesses these FIFOs by reading and writing to either the DFIFO push/pop regions or the DFIFO read/write debug region. FIFO access is governed by the following rules:

*   Read access to any address in any one of the 1 KB push/pop regions will result in a pop from the shared RX FIFO.
*   Write access to a particular 1 KB push/pop region will result in a push to the corresponding endpoint or channel’s TX FIFO given that the endpoint is an IN endpoint, or the channel is an OUT channel.

    -   In Device mode, data is pushed to the corresponding IN endpoint’s dedicated TX FIFO.
    -   In Host mode, data is pushed to the non-periodic TX FIFO or the periodic TX FIFO depending on whether the channel is a non-periodic channel, or a periodic channel.
*   Access to the 128 KB read/write region will result in direct read/write instead of a push/pop. This is generally used for debugging purposes only.

Note that pushing and popping data to and from the FIFOs by the CPU is only required in Slave mode. In DMA mode, the internal DMA will handle all pushing/popping of data to and from the TX and RX FIFOs.

### 50.4.3 FIFO and Queue Organization

The FIFOs in OTG_FS are primarily used to hold data packet payloads, i.e., the data field of USB Data packets. TX FIFOs are used to store data payloads that will be transmitted by OUT transactions in Host mode or IN transactions in Device mode. RX FIFOs are used to store received data payloads of IN transactions in Host mode or OUT transactions in Device mode. In addition to storing data payloads, RX FIFOs also store a **status entry** for each data payload. Each status entry contains information about a data payload such as channel number, byte count, and validity status. In Slave mode, status entries are also used to indicate various channel events.

The portion of SPRAM that can be used for FIFO allocation has a depth of 256 and a width of 35 bits (32 data bits plus 3 control bits). The multiple FIFOs used by each channel in Host mode or endpoint in Device mode are allocated into the SPRAM and can be dynamically sized.
```