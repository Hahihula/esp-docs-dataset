

```markdown
TX FIFO Stores the data to be transmitted.

Periodic FIFO Stores Isochronous transfer data and Interrupt transfer data to be sent.

Non-periodic FIFO Stores Control transfer data and Bulk transfer data to be sent.
```

## 49.3 Features

### 49.3.1 General Features

- USB 2.0 specification, OTG Revision 1.3 and OTG Revision 2.0 specifications
- High-Speed, Full-Speed, and Low-Speed data rates
- As a host and a device in High-Speed mode and Full-Speed mode
- Dynamic FIFO (DFIFO) sizing, each device EP/host channel can dynamically allocate a maximum of 4 KB FIFO.
- Multiple modes of memory access

    - Scatter/Gather DMA mode
    - Buffer DMA mode
    - Slave Mode

- Integrated UTMI High-Speed transceiver

### 49.3.2 Device Mode Features

- Endpoint 0 always present, bi-directional, consisting of EPO IN and EPO OUT
- 15 additional endpoints 1~15, configurable as IN or OUT
- Maximum of eight IN endpoints concurrently active at any time, including EPO IN
- All OUT endpoints share a single RX FIFO
- Each IN endpoint has a dedicated TX FIFO

### 49.3.3 Host Mode Features

- 16 host channels
- RX FIFO: shared by all periodic and non-periodic transactions
- Two TX FIFO:

    - One shared by all non-periodic transactions
    - One shared by all periodic transactions

- All of the above FIFOs share a 4 KB RAM.
- The size of each FIFO is configurable, with a maximum of 4 KB.
```