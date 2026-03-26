

```markdown
## 54.9.4 Initializing DMA Transmission

To initialize DMA transmission, perform the following steps:

1. The host sets up the descriptor fields (DESO-DES3) for transmission, and sets the OWNER bit (DESO[31]) to 1. The host also prepares the data buffer.
2. The host writes the write data command to the command register SDHOST_CMD_REG.
3. The host sets the required transmit threshold via the SDHOST_TX_WMARK field in the SDHOST_FIFOTH_REG register.
4. The DMA Controller engine fetches the descriptor and checks the OWNER bit. If the OWNER bit is not set, it means that the host owns the descriptor. In this case, the DMA Controller enters a suspend state and asserts the Descriptor Unable interrupt via the SDHOST_IDSTS_REG register. The host then needs to release the DMA Controller by writing any value to SDHOST_PLDMND_REG.
5. The DMA Controller waits for the Command Done (CMDD) bit in the SDHOST_RINTSTS_REG register to be set to 1 with no errors from BIU, which indicates that a transfer has completed.
6. The DMA Controller engine waits for a DMA interface request from BIU. This request is generated based on the configured transmit threshold value. For the last byte of data that cannot be accessed using a burst, a single transfer is performed on the AHB bus.
7. The DMA Controller fetches the transmit data from the data buffer in the host memory and transfers them to RAM in preparation for transmission to the card.
8. When data span across multiple descriptors, the DMA Controller fetches the next descriptor and continues with its operation with the next descriptor. The Last Descriptor bit indicates whether the data span multiple descriptors or not.
9. When data transmission is complete, the status information is updated in the SDHOST_IDSTS_REG register by setting the SDHOST_IDSTS_TI bit to 1 if it has already been enabled. Also, the OWNER bit is cleared by the DMA Controller by updating the DESO field.

## 54.9.5 Initializing DMA Reception

To initialize DMA reception, perform the following steps:

1. The host sets up the descriptor fields (DESO-DES3) for reception, and sets the OWNER bit (DESO[31]) to 1.
2. The host writes the read data command in the SDHOST_CMD_REG register in BIU.
3. The host sets the required receive threshold level via the SDHOST_RX_WMARK field in the SDHOST_FIFOTH_REG register.
4. The DMA Controller engine fetches the descriptor and checks the OWNER bit. If the OWNER bit is not set, it means that the host owns the descriptor. In this case, the DMA enters suspend state and asserts the Descriptor Unable interrupt via the SDHOST_IDSTS_REG register. The host then needs to release the DMA Controller by writing any value to SDHOST_PLDMND_REG.
5. The DMA Controller waits for the Command Done (CMDD) bit in the SDHOST_RINTSTS_REG register to be set to 1 with no errors from BIU, which indicates that a reception has been completed.
```