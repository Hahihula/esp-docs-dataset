

```markdown
Chapter 38 Controller Area Network Flexible Data-Rate (CAN FD) GoBack

19 REG32_WR(TX_COMMAND_ADDR, command); // Issue the command

When CAN FD is enabled by writing 1 to TWAIFD_ENA, it is still bus-off during integration onto the CAN bus. If during this time a "set ready" command is issued to TX buffer, and if TWAIFD_TBFBO = 1, the TX buffer will immediately move to the "aborted" state. Before issuing any "set ready" command to a TX buffer, software should wait until the node is error-active either by polling TWAIFD_EWL_ERP_FAULT_STATE_REG or via the FCS interrupt.

TX buffers are not initialized no reset. Therefore, before issuing the "set ready" command, software should fill the corresponding TX buffer with valid CAN frames for transmission.

CAN FD transmits only reactive overload frames. There are no internal conditions within CAN FD that would cause it to transmit an overload frame without overload being detected.

38.5.1.2 CAN Frame Reception

38.5.1.2.1 Sample Code 1 - Frame Reception in Automatic Mode (32-bit Access)

#define CAN_FD_BASE TWAIFD_DEVICE_ID_VERSION_REG
#define RX_DATA_ADDR (CAN_FD_BASE + 0x6C)
#define RX_STATUS_ADDR (CAN_FD_BASE + 0x68)

/* Poll on RX buffer until there is a frame in it */
uint32_t rx_status;
do {
    rx_status = REG32_RD(RX_STATUS_ADDR);
} while ((rx_status & 0x1) == 0)

/* Read the frame from RX buffer */
uint8_t data[64];
uint32_t tmp;
uint32_t fftw = REG32_RD(RX_DATA_ADDR);
uint32_t id = REG32_RD(RX_DATA_ADDR);
uint32_t ts_l = REG32_RD(RX_DATA_ADDR);
uint32_t ts_h = REG32_RD(RX_DATA_ADDR);
uint32_t rwcmt = (fftw >> 11) & 0x1F;
for(int i = 0; i < rwcmt; i++){
    tmp = REG32_RD(RX_DATA_ADDR);
    data[i*4] = tmp & 0xFF;
    data[i*4+1] = (tmp >> 8) & 0xFF;
    data[i*4+2] = (tmp >> 16) & 0xFF;
    data[i*4+3] = (tmp >> 24) & 0xFF;
}
```