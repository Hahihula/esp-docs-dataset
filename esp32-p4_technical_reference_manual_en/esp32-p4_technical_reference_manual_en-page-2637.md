

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC)
Register 52.3. DMARXPOLLDEMAND_REG (0x1008)

RECV_POLL_DEMAND Configures whether to enable the RX DMA to check if the DMA owns the current descriptor.
Any value: Enable
When this field is written, the DMA reads the current descriptor pointed to by DMARXCUR-RDESC_REG. If that descriptor is not available (owned by the Host), the reception returns to the Suspended state and the Bit 7 (RU) of Register 5 (Status Register) is not asserted. If the descriptor is available, the RX DMA returns to the active state.(RO/W/T)

Register 52.4. DMARXBASEADDR_REG (0x100C)

START_RECV_LIST Configures the base address of the first descriptor in the receive descriptor linked list.
The LSB bits (1:0) are ignored (32-bit wide bus) and internally taken as all-zero by the DMA. Therefore, these LSB bits are read-only (RO). (R/W)

Register 52.5. DMATXBASEADDR_REG (0x1010)

START_TRAN_LIST Configures the base address of the first descriptor in the Transmit Descriptor list. The LSB bits (1:0) are ignored (32-bit wide bus) and are internally taken as all-zero by the DMA. Therefore, these LSB bits are read-only (RO). (R/W)
```