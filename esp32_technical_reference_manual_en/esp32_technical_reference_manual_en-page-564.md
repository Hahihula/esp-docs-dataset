**Title: Chapter 26 SDIO Slave Controller (SDIO)**

---

### Figure Caption:
- **Figure 26.3-1. SDIO Slave Block Diagram**

The Host System represents any SDIO specification V2.0-compatible host device. The Host System interacts with the ESP32 (configured as the SDIO slave) via the standard SDIO bus implementation.

The SDIO Device Interface block enables effective communication with the external Host by directly providing SDIO interface registers and enabling DMA operation for high-speed data transfer over the Advanced High-performance Bus (AHB) without engaging the CPU.

---

**Subtitle: 26.3.2 Sending and Receiving Data on SDIO Bus**

Data is transmitted between Host and Slave through the SDIO bus I/O Function1. After the Host enables the I/O Function1 in the Slave, according to the SDIO protocol, data transmission will begin.
ESP32 segregates data into packets sent to/from the Host. To achieve high bus utilization and data transfer rates, we recommend the single block transmission mode. For detailed information on this mode, please refer to the SDIO V2.0 protocol specification. When Host and Slave exchange data blocks on the SDIO bus, the Slave automatically pads data-when sending data out-and automatically strips padding data from the incoming data block.

Whether the Slave pads or discards the data depends on the data address on the SDIO bus. When the data address is equal to, or greater than, 0x1F800, the Slave will start padding or discarding data. Therefore, the starting data address should be 0x1F800 - Packet_length, where Packet_length is measured in bytes. Data flow on the SDIO bus is shown in Figure **26.3-2**.

---

### Diagram Caption:
- **Figure 26.3-2. SDIO Bus Packet Transmission**

The standard IO_RW_EXTENDED (CMD53) command is used to initiate a packet transfer of an arbitrary length. The content of the CMD53 command used in data transmission is as illustrated in Figure **26.3-3** below.

---

### Diagram:
- A diagram showing "Packet block 0 CRC" and "block n CRC", with addresses labeled (e.g., Addr:0x1F800 - Packet_length).

---

For detailed information on CMD53, please refer to the SDIO protocol specifications. 

---

*Espressif Systems*

*Submit Documentation Feedback*

**Page Number:** 564  
**Document Version:** ESP32 TRM (Version 5.6)