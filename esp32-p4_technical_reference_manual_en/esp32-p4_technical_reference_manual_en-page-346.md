

```markdown
Figure 5.4-1. VDMA Architecture

It can be seen from the figure that:

* The CPU accesses VDMA registers via the APB3 slave interface.
* VDMA has four channels (Channel 1 to Channel 4). Each channel has a data FIFO with a depth of 64 and a width of 64 bits.
* VDMA has two AXI master interfaces (Master 1 and Master 2).
    * Master 1 can access ISP, MIPI DSI, and memory, as blue arrows indicate.
    * Master 2 can only access memory, as red arrows indicate.
    * Master 1 and Master 2 each have an arbiter that arbitrates read and write requests on all channels.
* VDMA has three hardware handshaking interfaces. Table 5.4-1 shows the mapping between the handshaking interfaces and peripherals.

Table 5.4-1. Hardware Handshaking Interface and Peripherals Mapping Table

| Handshaking Interface Number | Peripheral |
|-------------------------------|------------|
| 0                             | MIPI DSI   |
```