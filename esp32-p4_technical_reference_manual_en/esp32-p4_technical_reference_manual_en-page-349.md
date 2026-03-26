
```markdown
Chapter 5 VDMA Controller (VDMA)

5.5.2 Arbitration Scheme

The arbitration mechanism arbitrates read and write requests for all channels.

VDMA uses a priority and fair-among-equals arbitration mechanism. The priority for each channel is defined in the channel configuration register DMAC_CHn_CFG1_REG.

A priority of 3 is the highest, while 0 is the lowest. Multiple channels can share the same priority level.

The arbitration mechanism works as follows:

*   The arbitration mechanism determines which request client to grant the authorization signal based on the priority of the request. The request with the highest priority will be granted access to the channel.
*   When two or more requests have the same priority, request clients will gain access randomly.

5.5.2.1 Read Arbiter

The read arbiter arbitrates read requests, including:

*   VDMA’s read requests to obtain data or status from the source
*   VDMA’s read requests to obtain status from the destination
*   VDMA’s read requests to obtain LLI descriptors

The block diagram of the read arbiter is shown in Figure 5.5-3:
```mermaid
graph TD;
    subgraph Channels[Channel 1, Channel 2, Channel 3, Channel 4]
        Channel1[Source Data/Status Read Request<br>Destination Status Read Request<br>LLI Descriptor Read Request]
        Channel2[Source Data/Status Read Request<br>Destination Status Read Request<br>LLI Descriptor Read Request]
        Channel3[Source Data/Status Read Request<br>Destination Status Read Request<br>LLI Descriptor Read Request]
        Channel4[Source Data/Status Read Request<br>Destination Status Read Request<br>LLI Descriptor Read Request]
    end

    Channels -->|Read Arbiter| ReadArbiter
    ReadArbiter -- Read Request Grant --> ReadRequestGrant
    ReadArbiter -- Read Request Grant Index --> ReadRequestGrantIndex

    style Channel1 fill:#f9f,stroke:#333,stroke-width:2px;
    style Channel2 fill:#fff,stroke:#333,stroke-width:2px;
    style Channel3 fill:#fff,stroke:#333,stroke-width:2px;
    style Channel4 fill:#fff,stroke:#333,stroke-width:2px;

    ReadArbiter[Read Arbiter] as arbiter
```
Figure 5.5-3. VDMA Read Arbiter

Read requests to obtain linked list descriptors will be granted the highest priority, regardless of the channels' priority settings.
```