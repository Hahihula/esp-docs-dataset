

```markdown
Buffer DMA mode    Accesses contiguous memory areas via DMA.

Slave mode          Accesses memory area through the CPU.

RX FIFO             Stores the received data.

TX FIFO             Stores the data to be transmitted.

Periodic FIFO       Stores Isochronous transfer data and Interrupt transfer data to be sent.

Non-periodic FIFO   Stores Control transfer data and Bulk transfer data to be sent.
```

## 50.3 Features

### 50.3.1 General Features

- USB 2.0 specification, OTG Revision 1.3 and OTG Revision 2.0 specifications
- USB 2.0 full-speed and low-speed data rates
- HNP and SRP as A-device or B-device
- Dynamic FIFO (DFIFO) sizing, maximum to 1 KB
- Multiple modes of memory access
    - Scatter/Gather DMA mode
    - Buffer DMA mode
    - Slave mode
- Two integrated transceivers

### 50.3.2 Device Mode Features

- Endpoint 0 always present, bi-directional, consisting of EPO IN and EPO OUT
- Six additional endpoints 1~6, configurable as IN or OUT
- Maximum of five IN endpoints concurrently active at any time, including EPO IN
- All OUT endpoints share a single RX FIFO
- Each IN endpoint has a dedicated TX FIFO

### 50.3.3 Host Mode Features

- Eight host channels
- RX FIFO: shared by all periodic and non-periodic transactions
- Two TX FIFO:
    - One shared by all non-periodic transactions
    - One shared by all periodic transactions
- All of the above FIFOs share a 1 KB RAM.
- The size of each FIFO is configurable, with a maximum of 1 KB.
```