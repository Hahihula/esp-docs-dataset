

```markdown
| Address | Bit 7             | Bit 6              | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0                                                                 |
|---------|-------------------|--------------------|-------|-------|-------|-------|-------|------------------------------------------------------------------------|
|         |                   |                    |       |       |       |       | 0x2   | (Function 2 Standard SDIO Function interface code)                     |
| 0x200   | 0                 | (Function 2 CSA enable) | 0     | O     | RFU   |       |       |                                                                        |
|         |                   |                    |       |       |       |       |       |                                                                        |
| 0x201   |                   |                    |       |       | O     |       |       | (Function 2 Extended standard SDIO Function interface code)            |
| 0x202   |                   |                    |       | O     | RFU   |       | R/W   | O                                                                      |
|         |                   |                    |       |       |       |       | (EPS) | (SPS)                                                                   |
| 0x209-0x20B |               | Address 0x209: 0x0; Address 0x20A: 0x12; Address 0x20B: 0x0<br>(Pointer to Function 2 CIS) |
| 0x210-0x211 |               | R/W (Supported range: 0-512)<br>(I/O block size for Function 2)       |       |       |       |       |       |                                                                        |

**Table 39.5-2. SDIO Slave FBR Configuration – cont’d from previous page**

## 39.5.4 I/O Function 1/2 Address Space Map

I/O function 1 and function 2 have identical functions and permissions. They can be used simultaneously or independently to transmit application data (such as Wi-Fi or Bluetooth data) in fixed-address packets or incremental-address packets. Both functions can access the same set of SLC Host registers. Figure 39.5-4 shows their address space map. All segments in this space can be accessed by the host.

| 0x0      | Fixed address Packet |
|----------|----------------------|
| 0x1 -0x3F | Reserved             |
| 0x40 -0x3FF | SLC Host Register   |
| 0x400 - 0x1F7FF | Incr address Packet |

**Figure 39.5-4. Function 1/2 Address Space Map**

### 39.5.4.1 Accessing SLC HOST Register Space

The host can access registers in the contiguous address range from 0x40 to 0x3FF in the slave via I/O functions 1 or 2. To access these registers, the host sets the Register Address field of CMD52 or CMD53 to the low 10 bits of the address. CMD53 also allows the host to access multiple registers in a single operation for higher transfer rates.

From SLCHOST_CONF_WO_REG and SLCHOST_CONF_W15_REG, there are 52 bytes of fields accessible and modifiable by both the host and slave, facilitating information exchange.

Both host and slave software can access the SLC Host register space simultaneously. Therefore, an upper-layer mechanism should be implemented to prevent errors caused by concurrent access.
```