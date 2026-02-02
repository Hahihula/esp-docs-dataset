**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Body Text:**

Check Sequence) field used to verify the CRC for the frame. The received frame is stored in a shallow buffer until the address filtering is performed. The frame is dropped in the MAC if it fails the address filtering.

The frame received by the MAC will be pushed into the Rx FIFO. Once the FIFO status exceeds the Receive Threshold, configured by the Receive Threshold Control (RTC) bit in the Operation Mode register, the DMA can initiate a preconfigured burst transmission to the AHB interface.

In the default pass-through mode, when the FIFO receives a complete packet or 64 bytes configured by the RTC bit in the Operation Mode register, the data pops up and its availability is notified to the DMA. After the DMA initiates the transmission to the AHB interface, the data transmission continues from the FIFO until the complete packet is transmitted. Upon completing transmitting the EOF, the status word will pop up and be transmitted to the DMA controller.

In the Rx FIFO Store-and-Forward mode (configured through the RSF or Receive Store and Forward bit in the Operation Mode Register), only the valid frames are read and forwarded to the application. In the passthrough mode, error frames are not discarded because the error status is received at the end of the frame. The start of frame will have been read from the FIFO at that point.

**Subsection Title:**
24.2.2.1 Reception Protocol

After the receive module receives the packets, the Preamble and SFD of the received frames are removed. When the SFD is detected, the MAC starts sending Ethernet frame data to the Rx FIFO, starting at the first byte (destination address) following the SFD.

If the received frame length/type is less than 0x600 and the automatic CRC/Pad removal option is programmed for the MAC, the MAC will send frame data to the Rx FIFO (the amount of data does not exceed the number specified in the length/type field). Then MAC begins discarding the remaining section, including the FCS field. If the frame length/type is greater than, or equal to, 0x600, the MAC will send all received Ethernet frame data to the Rx FIFO, regardless of the programmed value of the automatic CRC removal option.

By default, the MAC watchdog timer is enabled, meaning that frames, including DA, SA, LT, data, pad and FCS, which exceed 2048 bytes, are cut off. This function can be disabled by programming the Watchdog Disable (WD) bit in the MAC Configuration Register. However, even if the watchdog timer is disabled, frames longer than 16 KB will be cut off and the watchdog timeout status will be given.

**Subsection Title:**
24.2.2.2 Receive Frame Controller

If the RA (Receive All) bit in the MAC Frame Filter Register is reset, the MAC will filter frames based on the destination and source addresses. If the application decides not to receive any bad frames, such as runt frames and CRC error frames, another level of filtering is needed. When a frame fails the filtering, the frame is discarded and is not transmitted to the application. When the filter parameters are changed dynamically, if a frame fails the DA and SA filters, the remaining part of the frame is discarded and the Receive Status word is updated immediately and, therefore, the zero frame length bit, CRC error bit, and runt frame error bit are set to 1. This indicates that the frame has failed the filtering.

**Subsection Title:**
24.2.2.3 Receive Flow Control

The MAC will detect the received pause frame and pause transmission of frames for a specified delay within the received pause frame (in full-duplex mode only). The Pause Frame Detect Function can be enabled or disabled by the RFCE (Receive Flow Control Enable) bit in the Flow Control Register. When receive flow control is enabled, it starts monitoring whether the destination address of the received frame matches the

**Footer:**
Espressif Systems
465 ESP32 TRM (Version 5.6)
Submit Documentation Feedback