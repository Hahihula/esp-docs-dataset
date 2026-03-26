

```markdown
pointer to the data payload or buffer and a 32-bit buffer descriptor (BufferStatus Quadlet). The data payloads and buffers can correspond to a single transaction (i.e., < 1 MPS bytes) or an entire transfer (> 1 MPS bytes). MPS: maximum packet size. The list is implemented as a ring buffer meaning that the DMA will return to the first entry when it encounters the last entry on the list.

* When transmitting a transfer/transaction using IN endpoints or OUT channels, the DMA will gather the data payloads from the multiple buffers and push them into a TX FIFO.
* When receiving a transfer/transaction using OUT endpoints or IN channels, the DMA will pop the received data payloads from the RX FIFO and scatter them to the multiple buffers pointed to by the DMA list entries.

## 49.4.6 Transaction and Transfer Level Operation

In either Host or Device mode, communication can operate either at the transaction level or the transfer level.

### 49.4.6.1 Transaction and Transfer Level Operation in DMA Mode

When operating at the transfer level in DMA Host mode, software is interrupted only when a channel has been halted. Channels are halted when their programmed transfer size has completed successfully, has received a STALL, or if there are excessive transaction errors, e.g., 3 consecutive transaction errors. In DMA Device mode, all errors are handled by the controller core itself.

When operating at the transaction level in DMA mode, the transfer size is set to the size of one data packet, either a maximum packet size or a short packet size.

### 49.4.6.2 Transaction and Transfer Level Operation in Slave Mode

When operating at the transaction level in Slave Mode, transfers are handled one transaction at a time. Each data payload should correspond to a single data packet, and software must determine whether a retry of the transaction is necessary based on the handshake response received on the USB, e.g., ACK or NAK.

The following table describes transaction level operation in Slave mode for both IN and OUT transactions.

Table 49.4-1. IN and OUT Transactions in Slave Mode

| Host Mode | Device Mode |
|-----------|-------------|
| OUT Transactions |           |
```