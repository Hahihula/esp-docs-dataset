

```markdown
Figure 49.4-3. Host Mode FIFOs

*   Non-periodic TX FIFO: Stores data payloads of bulk and control OUT transactions for all channels.
*   Periodic TX FIFO: Stores data payloads of interrupt or isochronous OUT transactions for all channels.
*   RX FIFO: Stores data payloads of all IN transactions, and status entries that are used to indicate size of data payloads and transaction/channel events such as transfer complete or channel halted.

In addition to FIFOs, Host mode also contains two request queues used to queue up the various transaction request from the multiple channels. Each entry in a request queue holds the IN/OUT channel number along with other information to perform the transaction, such as transaction type. Request queues are also used to queue other types of requests such as a channel halt request.

Unlike FIFOs, request queues are fixed in size and cannot be accessed directly by software. Rather, once a channel is enabled, requests will be automatically written to the request queue by the Host core. The order in which the requests are written into the queue determines the sequence of transactions on the USB.

Host mode contains the following request queues:

*   Non-periodic request queue: Request queue for all non-periodic Bulk and Control channels. The queue has a depth of four entries.
*   Periodic request queue: Request queue for all periodic Interrupt and Isochronous channels. The queue has a depth of four entries.

When scheduling transactions, hardware will execute all requests on the periodic request queue first before executing requests on the non-periodic request queue.

49.4.3.2 Device Mode FIFOs

The following FIFOs are used in Device mode, see Figure 49.4-4:
```