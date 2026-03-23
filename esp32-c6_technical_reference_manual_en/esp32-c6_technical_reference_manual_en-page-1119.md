

```markdown
Chapter 34 SDIO Slave Controller (SDIO)

GoBack

34.7 Packet Sending and Receiving Procedure

The SDIO host and slave devices need to follow specific data transfer procedures to successfully exchange data over the SDIO interface. Beside SDIO Specifications, ESP32-C6 should also follow the procedures below to transmit data over higher abstraction layers, such as Wi-Fi and Bluetooth data.

34.7.1 Sending Packets to SDIO Host

The transmission of packets from the slave to the host is initiated by the slave. The host will be notified with an interrupt (for detailed information on interrupts, please refer to SDIO Specification). After the host reads the relevant information from the slave, it will initiate an SDIO bus transmission accordingly. The whole procedure is illustrated in Figure 34.7-1.

Figure 34.7-1. Procedure of Slave Sending Packets to Host

1. The slave CPU creates the linked list for the data packets that it will send to the host. For how to create a linked list, please refer to Section 34.5.5.1.
2. The slave CPU updates the length of data that will be sent to the host using the register
```