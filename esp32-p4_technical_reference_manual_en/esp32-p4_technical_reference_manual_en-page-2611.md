

```markdown
Table 52.4-5. Transmit Descriptor 6 (TDES6)

| Bits   | Name                          | Description                                                                                                                                                                                                 |
|--------|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [31:0] | TTSL: Transmit Frame Time Stamp Low | This field is updated by DMA with the least significant 32 bits of the timestamp captured for the corresponding transmit frame. This field has the timestamp only if the Last Segment (TDES0[29]) bit in the descriptor is set, and the Timestamp Status (TDES0[17]) bit is set. |

Table 52.4-6. Transmit Descriptor 7 (TDES7)

| Bits   | Name                          | Description                                                                                                                                                                                                 |
|--------|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [31:0] | TTSH: Transmit Frame Time Stamp High | This field is updated by DMA with the most significant 32 bits of the timestamp captured for the corresponding receive frame. This field has the timestamp only if the Last Segment (TDES0[29]) bit in the descriptor is set, and the Timestamp Status (TDES0[17]) bit is set. |

52.4.3.2 Receive Descriptors

Figure 52.4-2 shows the structure of the receive descriptor linked list. Table 52.4-7 through Table 52.4-11 show the descriptions of each receive descriptor.

![Figure 52.4-2. Receive Descriptor Linked List](image)

Table 52.4-7. Receive Descriptor 0 (RDES0)

| Bits | Name          | Description                                                                                                                                                                                                 |
|------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [31] | OWN: Own Bit  | When set, this bit indicates that the descriptor is owned by the DMA. When reset, it indicates that the descriptor is owned by the Host. The DMA clears this bit either when it completes the frame reception or when the buffers that are associated with this descriptor are full. |
```