**Chapter Title:**
Chapter 26 SDIO Slave Control (SDIO)

**Table Header for Figure 26.3-3: CMD53 Content**

| Command Index | R/W flag | Function Number | Block Mode Code | Register Address | Byte/Block Count | Roundup |
|---------------|----------|-----------------|-----------------|------------------|------------------|---------|
| S D           |         | 1               | 0x1F800-Packet_length (Packet_length/Block_size) | CRC7 E          |                   |

**Subsection Title:**
26.3.3 Register Access

**Body Text:**
For effective interaction between Host and Slave, the Host can access certain registers in the Slave via the SDIO bus I/O Function1. These registers are in continuous address fields from SLCOHOST_TOKEN_RDATA to SSLCOHOST_INT_ST_REG. The Host device can access these registers by simply setting the register addresses of CMD52 or CMD53 to the low 10 bits of the corresponding register address. The Host can access several consecutive registers at one go with CMD53, thus achieving a higher effective transfer rate.

There are 52 bytes of field between SLCHOST_CONF_WO_REG and SLCHOST_CONF_W15_REG. Host and Slave can access and change these fields, thus facilitating the information interaction between Host and Slave.

**Subsection Title:**
26.3.4 DMA

**Body Text:**
The SDIO Slave module uses dedicated DMA to access data residing in the RAM. As shown in Figure 26.3-1, the RAM is accessed over the AHB. DMA accesses RAM through a linked-list descriptor. Every linked list is composed of three words, as shown in Figure 26.3-4.

**Figure Caption:**
Figure 26.3-4. SDIO Slave DMA Linked List Structure

| Owner | Eof | Reserved | Length | Size |
|-------|-----|----------|--------|------|
|       |     |          |        |      |

**Table Header for Figure 26.3-4:**
Buffer Address Pointer
Next Descriptor Address

**Body Text (continued):**
Owner:
- The allowed operator of the buffer that corresponds to the current linked list. O: CPU is the allowed operator; 1: DMA is the allowed operator.

Eof:
- End-of-file marker, indicating that this linked-list element is the last element of the data packet.

Length:
- The number of valid bytes in the buffer, i.e., the number of bytes that should be accessed from the buffer for reading/writing.

Size:
- The maximum number of available buffers.

Buffer Address Pointer:
- The address of the data buffer as seen by the CPU (according to the RAM address space).

Next Descriptor Address:
- The address of the next linked-list element in the CPU RAM address space. If the current linked list is the last one, the Eof bit should be 1, and the last descriptor address should be O.

The Slave's linked-list chain is shown in Figure 26.3-5:

**Footer:**
Espressif Systems
Page number: 565

**Link Texts:**
GoBack
Figure 26.3-4.
Submit Documentation Feedback