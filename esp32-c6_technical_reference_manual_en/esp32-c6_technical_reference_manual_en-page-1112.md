

```markdown
34.5.4 I/O Function 1/2 Address Space Map

I/O function 1 and 2 have the exactly the same functions and permissions. They can be used at the same time or independently to transmit application data (such as Wi-Fi data and Bluetooth data) in fixed-address packets or incremental-address packets. They can also access the same set of SLC Host registers. Figure 34.5-4 shows their address space map. All segments in this space can be accessed by the host.

| 0x0 | Fixed address Packet |
|-----|----------------------|
| 0x1 - 0x3F | Reserved |
| 0x40 - 0x3FF | SLC Host Register |
| 0x400 - 0x1F7FF | Incr address Packet |

Figure 34.5-4. Function 1/2 Address Space Map

34.5.4.1 Accessing SLC HOST Register Space

For effective interaction, the host can access the registers that are in contiguous address from 0x40 to 0x3FF in the slave via the I/O function 1/2. To access them, the host simply needs to set the Register Address field of CMD52 or CMD53 to the low 10 bits of their address. Besides, CMD53 allows the host to access multiple registers at one go for a higher transfer rate.

From SLCHOST_CONF_WO_REG and SLCHOST_CONF_W15_REG, there are 52 bytes of fields that the host and slave can access and change, thus facilitating the information interaction.

The software on both the host and the slave sides can access the SLC Host register space at the same time, so an upper-layer mechanism should be designed to avoid the error caused by such behavior.

34.5.4.2 Transferring Incremental-Address Packets

When the host uses the address 0x400 - 0x1F7FF to continuously transmit multiple application data packets (such as Wi-Fi packets), the address field in CMD53 should be set to increment mode and the OP Code field to 1.

For example, if the host wants to use CMD53 to transfer (send or receive) three data blocks starting from the base address 0x500, then it should:

* Set the Block Mode field in CMD53 to 1, indicating data unit is block
* Set the OP Code field to 1, indicating incremental address mode
* Set the Register Address field to 0x500, indicating the base address is 0x500
* Set the Byte/Block Count field to 0x3, indicating 3 data blocks
* Set other fields according to the SDIO Specification

When the packet is transmitted (slave sends to host, or slave receives from host) through CMD53, the slave will determine whether all the valid data of the current packet has been transmitted so as to pad (when slave sends to host) or discard (when slave receives from host) the invalid data. For more information about data padding and discarding, please refer to Section 34.5.5.3.
```