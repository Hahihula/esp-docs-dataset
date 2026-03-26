

```markdown
Chapter 54 SD/MMC Host Controller (SDHOST)

- debounce filter (SDHOST_DEBNCE_REG)
- internal phase shift (SDHOST_ENSHIFT_REG)

You can reset the card with SDHOST_RST_N_REG.

## 54.9.2 Sending Commands

To send commands, perform the following steps:

1. Write the command argument register `SDHOST_CMDARG_REG` with the appropriate command argument parameter.
2. For data transfer, write the data size register `SDHOST_BYTCNT_REG`, the block size register `SDHOST_BLKSIZ_REG` register, and the card threshold control register `SDHOST_CARDTHRCTL_REG` to configure data transfer parameters.
3. Data transfer can be achieved by DMA or FIFO, and DMA is preferable.

    - To transmit and receive data via DMA, configure the DMA Controller according to Section 54.9.3, Section 54.9.4, and Section 54.9.5.
    - To transmit and receive data via FIFO, configure the FIFO threshold via FIFO configuration register `SDHOST_FIFOTH_REG`. For writing to a card, software should write data to the FIFO via `SDHOST_BUFFIFO_REG` continuously during command execution.

4. Configure and start the command via the `SDHOST_CMD_REG`.

5. Wait until the `SDHOST_START_CMD` bit in the `SDHOST_CMD_REG` register is cleared by hardware upon command reception. When hardware cannot receive the command, it will set the 12th bit HLE in the `SDHOST_RINTSTS_REG` register to 1.

6. Read the `SDHOST_RINTSTS_REG` register or enable interrupts to check command execution status. If needed, read the `SDHOST_RESPn_REG` (`n` ranges from 0 ~ 3) register to get command response from the card.

7. If data is read from the card via FIFO, software can get the data returned by the card via reading the `SDHOST_BUFFIFO_REG` register.

Please refer to the card specification for the command format, and configure register field values depending on the command format.

## 54.9.3 Initializing DMA

To initialize the DMA Controller, perform the following steps:

1. Write to the DMA bus mode register (`SDHOST_BMOD_REG`) to configure the host bus’s access parameters.
2. Write to the DMA interrupt enable register (`SDHOST_IDINTEN_REG`) to mask unnecessary interrupt causes.
3. Create either a transmit or receive linked list. Then write the starting address of the first descriptor in the linked list to the DMA Controller’s linked list base address register (`SDHOST_DBADDR_REG`).
4. The DMA Controller engine proceeds to get descriptors from the linked list.

Espressif Systems
2739
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY
```