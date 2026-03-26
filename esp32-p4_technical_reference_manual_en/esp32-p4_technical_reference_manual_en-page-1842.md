

```markdown
Figure 39.5-2. H264_DMA Architecture

The functions of each module are:

*   register: This module implements register configuration and selection.
*   in_dscr: This module initiates an AXI read request to internal memory, obtains the RX channel’s linked list descriptor, and sends the descriptor to the in_link module of the corresponding RX channel.
*   in_link: This module receives the descriptor of the corresponding channel in_dscr module and splits it into multiple AXI write data requests to guide the corresponding in_fifo module to write data to internal memory or external memory. RX channel 0/1/4 is designed for writing data to external memory, while RX channel 2/3/5 is for writing data to internal memory.
*   in_fifo: Stores data transmitted by the h264 module or TX Channels 3/4, and waits for the AXI host to read the data from the corresponding channel. Specifically, the in_fifo of RX Channels 0/1/2/3/4 stores the data sent by the h264 module, while the in_fifo of RX Channel 5 stores the data transmitted by TX Channels 3/4.
*   out_dscr: This module initiates an AXI read internal memory request, obtains the TX channel linked list descriptor, and sends the descriptor to the out_link module of corresponding TX channel.
*   out_link: This module receives the descriptor of the corresponding channel out_dscr module and divides it into multiple AXI read data requests to obtain data from internal memory or external memory. TX channel 0/3/4 reads data from external memory and TX channel 1/2 reads data from internal memory.
```