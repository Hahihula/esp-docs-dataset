

```markdown
Figure 49.4-2. OTG_HS Register Layout

| Address Range | Description |
|---------------|-------------|
| 0000h         | Core Global CSRs (1 KB) |
| 0400h         | Host Mode CSRs (1 KB) |
| 0800h         | Device Mode CSRs (1 KB) |
| 0E00h         | Power and Clock Gating CSRs (1 KB) |
| 1000h         | Device EP0 / Host Channel 0 FIFO (4 KB) |
| 2000h         | Device EP1 / Host Channel 1 FIFO (4 KB) |
| 3000h         | Device EP n / Host Channel n FIFO (4 KB) |
|               | DFIFO push/pop to this region only for Slave mode |
| 20000h        | Reserved |
| 3FFFFh        | Direct Access to Data FIFO RAM for Debugging (128 KB) |
|               | DFIFO debug read/write to this region |

49.4.2.1 Control & Status Registers (CSRs)

- Core Global CSRs
These registers are responsible for the configuration/control/status of the global features of OTG_HS, i.e., features which are common to both Host and Device modes. These features include OTG control and system-level interrupts. Software can access these registers whilst in Host or Device modes.

- Host Mode CSRs
These registers are responsible for the configuration/control/status in Host mode, thus should only be accessed in Host mode. Each channel has its own set of registers within the Host mode CSRs.

- Device Mode CSRs
These registers are responsible for the configuration/control/status in Device mode, thus should only be accessed in Device mode. Each endpoint has its own set of registers within the Device mode CSRs.

- Power and Clock Gating Register
A single register controls power-down and gates various clocks.

49.4.2.2 FIFO Access

The OTG_HS makes use of multiple FIFOs to buffer the data payloads to be transmitted or to buffer the received data payloads. The number and type of FIFOs are dependent on Host or Device mode, and the number of channels or endpoints used, see Section 49.4.3. There are two ways to access the FIFOs: DMA mode and Slave mode. In Slave mode, the CPU will need to access these FIFOs by reading and writing to either the DFIFO push/pop regions or the DFIFO read/write debug region. FIFO access is governed by the
```