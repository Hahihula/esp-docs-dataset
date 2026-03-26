

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC) GoBack


52.4.1.2 Reception

A receive operation is initiated when the MAC detects an SFD on the RMII or MII. The MAC strips the preamble and SFD before proceeding to process the frame. The header fields are checked for filtering and the FCS (Frame Check Sequence) field used to verify the CRC for the frame. The received frame is stored in a shallow buffer until the address filtering is performed. The frame is dropped in the MAC if it fails the address filtering.

The frames received by the MAC are pushed into the RX FIFO. Once the RX FIFO crosses the configured Receive threshold (RX_THRESH_CTRL), its status is indicated to the DMA, so that the DMA can initiate a pre-configured burst transfers towards the AHB interface.

In the default cut-through mode, when the FIFO receives 64 bytes or a full packet of data, it pops out the data and indicates the availability to the DMA. Once the DMA initiates the transfer to the AHB interface, the data transmission continues from the FIFO until a complete packet has been transferred. Upon the completion of the EOF frame transfer, the status word will be popped out and transmitted to the DMA controller.

Receive Protocol

The receive module strips the preamble and SFD of the received frame. Once the SFD is detected, the MAC begins sending the Ethernet frame data to the RX FIFO, starting from the first byte following the SFD (destination address). If the IEEE 1588 timestamp feature is enabled, the snapshot of system time will be captured whenever an SFD of any frame is detected on MII, and sent to the application unless the MAC filters out and drops the frame.

If the Length/Type field of the receiving frame is less than 0x600 and if the MAC is programmed for the automatic CRC/paddingstripping option, the MAC sends the frame data up to the count specified in the Length/Type field to the RX FIFO, and then starts dropping bytes (including the FCS field). If the Length/Type field is greater than or equal to 0x600, the MAC will send all received Ethernet frame data to the RX FIFO, regardless of the value on the programmed automatic CRC stripping option. By default, the MAC is programmed for the watchdog timer to be enabled, that is frames above 2048 bytes (including DA, SA, LT, data, padding, and FCS) are cut off. This feature can be disabled by programming the Watchdog Disable bit EMACWATCHDOG. However, even if the watchdog timer is disabled, frames longer than 16 KB will still be cut off and the watchdog timeout status will be indicated.

Receive Frame Controller

If the RECEIVE_ALL bit in the MAC Frame Filter Register is reset, the MAC performs frame filtering based on the destination and source addresses. The application still needs to perform another level of filtering if it decides not to receive any bad frames like runt, CRC error frames, etc. On detecting a filter failure, the frame is dropped and not transmitted to the application. When the filter parameters change dynamically, if a DA and SA filter failure occurs, the reset of the frame is dropped and the Receive Status word (with zero frame length, CRC Error, and Runt Error bits set) is updated immediately indicating the filter failure.

Receive Flow Control

The MAC detects the receiving pause frame and pauses the frame transmission for the delay specified within the received pause frame (in full-duplex mode only). The Pause Frame Detection Function can be enabled or disabled with the RFCE bit. Once the receive flow control is enabled, the MAC starts monitoring the received frame destination address for any match with the multicast address of the control frame (0x0180 C200 0001).
```