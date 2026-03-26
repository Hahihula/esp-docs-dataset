

```markdown
## 52.4.3 EMAC_DMA

EMAC has its own DMA module, with independent Transmit and Receive engines and a CSR (Control and Status Registers) space. The Transmit engine transfers data from the system memory to the device port (MTL), while the Receive engine transmits data from the device port to the system memory. The controller uses descriptors to efficiently move data from source to destination with minimal Host CPU intervention. The DMA is designed for packet-oriented data transfer such as frames in Ethernet. The controller can be programmed to interrupt the Host CPU for normal situations, such as the completion of frame transmission or reception, or error conditions.

### 52.4.3.1 Transmit Descriptors

Figure 52.4-1 shows the structure of the transmit descriptor linked list. Table 52.4-1 through Table 52.4-4 show the descriptions of each transmit descriptor.

![Figure 52.4-1. Transmit Descriptor Linked List](image)

**Table 52.4-1. Transmit Descriptor O (TDESO)**

| Bits | Name                  | Description |
|------|-----------------------|-------------|
| [31] | OWN: Own Bit          | When set, this bit indicates that the descriptor is owned by the DMA. When reset, it indicates that the descriptor is owned by the Host. The DMA clears this bit, either when it completes the frame transmission or when the buffers allocated to the descriptor are empty. The ownership bit of the First Descriptor of the frame should be set after all subsequent descriptors belonging to the same frame have been set. This avoids a possible race condition between fetching a descriptor and the driver setting an ownership bit. |
| [30] | IC: Interrupt on Completion | When set, this bit sets the Transmit Interrupt TRANS_INT after the present frame has been transmitted. This bit is valid only when the last segment bit TDESO[29] is set. |
| [29] | LS: Last Segment      | When set, this bit indicates that the buffer contains the last segment of the frame, and the TBS1 or TBS2 field in TDES1 should have a non-zero value. |
```