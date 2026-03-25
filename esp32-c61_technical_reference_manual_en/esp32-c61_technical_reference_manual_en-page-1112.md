

```markdown
30.6.2 Slave Interrupt

* SLCO/1_TX_DSCR_ERR_INT : Slave TX linked list descriptor error.
* SLCO/1_RX_DSCR_ERR_INT : Slave RX linked list descriptor error.
* SLCO/1_RX_EOF_INT : Slave RX operation is finished.
* SLCO/1_RX_DONE_INT : A single buffer is received by the slave.
* SLCO/1_TX_SUC_EOF_INT : Slave TX operation is finished.
* SLCO/1_TX_DONE_INT : A single buffer is finished during TX operation.
* SLCO/1_TX_OVF_INT : Slave TX buffer overflow interrupt.
* SLCO/1_RX_UDF_INT : Slave RX buffer underflow interrupt.
* SLCO/1_TX_START_INT : Slave TX start interrupt.
* SLCO/1_RX_START_INT : Slave RX start interrupt.
* SLC_FRHOST_BITn_INT (n: 0–15): The host interrupts the slave via the SLCO channel if interrupt vector Bit[7:0] is set or via the SLC1 channel if interrupt vector Bit[15:8] is set.

30.7 Packet Sending and Receiving Procedure

The SDIO host and slave devices must follow specific data transfer procedures to successfully exchange data over the SDIO interface. In addition to SDIO Specifications, ESP32-C61 should also follow the procedures below to transmit data over higher abstraction layers, such as Wi-Fi and Bluetooth.

30.7.1 Sending Packets to SDIO Host

The transmission of packets from the slave to the host is initiated by the slave. The host is notified with an interrupt (for details, refer to the SDIO Specification). After the host reads the relevant information from the slave, it initiates an SDIO bus transmission accordingly. The procedure is illustrated in Figure 30.7-1.
```