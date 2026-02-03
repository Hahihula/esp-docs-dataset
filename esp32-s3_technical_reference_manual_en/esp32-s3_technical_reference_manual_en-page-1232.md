**Chapter Title:**
Chapter 32 USB On-The-Go (USB)

**Body Text:**

When channel is enabled, requests will be automatically written to the request queue by the Host core. The order in which the requests are written into the queue determines the sequence of transactions on the USB.

Host mode contains the following request queues:

- **Non-periodic request queue:** Request queue for all non-periodic channels (bulk and control). The queue has a depth of four entries.
  
- **Periodic request queue:** Request queue for all periodic channels (interrupt and isochronous). The queue has a depth of eight entries.

When scheduling transactions, hardware will execute all requests on the periodic request queue first before executing requests on the non-periodic request queue.

**Subsection Title:**
32.3.3.2 Device Mode FIFOs

**Diagram Description (Figure 32.3-4):**

The diagram shows a block structure for "Device Mode FIFOs" with various components and their relationships:

1. **MAC Pop -> AHB Push to TX FIFO #n Control**
   - This is connected through an arrow labeled `USB_INEPnTXFDEP`
   
2. **TX FIFO #n Data**:
   - Connected via arrows pointing towards the next level, indicating a flow of data.

3. **TX FIFO #1 Control -> AHB Push to TX FIFO #0 Control**
   - This is connected through an arrow labeled `USB_INEP1TXFDEP`
   
4. **TX FIFO #1 Data**:
   - Connected via arrows pointing towards the next level, indicating a flow of data.

5. **TX FIFO #0 Control -> AHB Push to RX FIFO Control**
   - This is connected with labels like `USB_NPTXKFSTADDR`, `USB_NPTXFDEP`, and `USB_RXFDEP`
   
6. **RX FIFO Control**:
   - Connected via arrows pointing towards the next level, indicating a flow of data.

7. **RX Data**
   - This is connected with labels like `USB_INEP1TXFSTADDR` (indicating RX starting address fixed to 0)

**Additional Text:**

The following FIFOs are used when operating in Device mode (See Figure 32.3-4):

- **RX FIFO:** Stores data payloads received in Data packet, and status entries (used to indicate size of those data payloads).
  
- **Dedicated TX FIFO:** Each active IN endpoint will have a dedicated TX FIFO used to store all IN data payloads of that endpoint, regardless of the transaction type (both periodic and non-periodic IN transactions).

Due to the dedicated FIFOs, Device mode does not use any request queues. Instead, the order of IN transactions are determined by the Host.

**Footer:**
Espressif Systems
1232 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback