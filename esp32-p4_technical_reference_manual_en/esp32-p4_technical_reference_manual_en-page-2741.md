

```markdown
6. The DMA Controller engine waits for a DMA interface request from BIU. This request is generated based on the configured receive threshold value. For the last byte of data that cannot be accessed using a burst, a single transfer is performed on the AHB bus.
7. The DMA Controller fetches the data from RAM and transfers them to the host memory.
8. When data span across multiple descriptors, the DMA Controller fetches the next descriptor and continues with its operation with the next descriptor. The Last Descriptor bit indicates whether the data span multiple descriptors or not.
9. When data reception is complete, the status information is updated in the SDHOST_IDSTS_REG register by setting the SDHOST_IDSTS_RI bit to 1, if it has already been enabled. Also, the OWNER bit is cleared by the DMA Controller by updating the DESO field.

## 54.10 Clock Phase Selection

The phase of the SD/MMC Host Controller clock source is configurable, so as to adjust the setup time sequence for the input or output data signals.

The clock source of the SD/MMC Host Controller can be a high-performance clock at a high frequency or a low-power clock at a low frequency. When the clock source is a high-performance clock, the internal signal clock phase, output signal driving clock phase, and input signal sampling clock phase can be configured via the SDHOST_DLL_CLK_CONF_REG, in the unit of 1/64 clock source period. When the clock source is a low-power clock, the internal signal clock phase, output signal driving clock phase, and input signal sampling clock phase can be configured via the system clock register. The phase options are 0 degrees, 90 degrees, 180 degrees, and 270 degrees, or in other words the unit is 1/4 clock source period.

For details, please see Chapter 10 Reset and Clock.

## 54.11 Interrupt

The SD/MMC Host Controller can generate interrupt signal SDIO_HOST_INTR triggered by the following interrupt sources, and send the interrupt signals to the Interrupt Matrix.

*   SDIO_INT: Interrupts from SDIO cards
*   EBE: Triggered when an error in end bit occurs, or no data CRC received
*   ACD: Triggered when an automatically sent command has been executed
*   SBE/BCI: Triggered when an error in the start bit occurs
*   HLE: Triggered when a write error occurs during hardware-lock period
*   FRUN: Triggered when the FIFO is empty or full
*   HTO: Triggered when the host does not fill data before timeout period
*   DRTO: Triggered when a data read operation times out
*   RTO: Triggered when card response times out
*   DCRC: Triggered when data CRC error occurs
*   RCRC: Triggered when a card response CRC error occurs
```