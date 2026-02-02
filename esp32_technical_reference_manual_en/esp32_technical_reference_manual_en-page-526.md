**Chapter Title:**
25 Two-Wire Automotive Interface (TWAI)

**Sub-chapter Navigation Menu:**
- Error Code Capture
- Arbitration Lost Capture

**Section 25.3 Functional Protocol**

**Subsection 25.3.1 TWAI Properties**

The TWAI protocol connects two or more nodes in a bus network, and allows for nodes to exchange messages in a latency bounded manner. A TWAI bus will has the following properties.

- **Single Channel and Non-Return-To-Zero:** The bus consists of a single channel to carry bits, thus communication is half-duplex. Synchronization is also derived from this channel, thus extra channels (e.g., clock or enable) are not required. The bit stream of a TWAI message is encoded using the Non-Return-to-Zero (NRZ) method.

- **Bit Values:** The single channel can either be in a Dominant or Recessive state, representing a logical 0 and a logical 1 respectively. A node transmitting a Dominant state will always override another node transmitting a Recessive state. The physical implementation on the bus is left to the application level to decide (e.g., differential wiring).

- **Bit-Stuffing:** Certain fields of TWAI messages are bit-stuffed. A Transmitter that transmits five consecutive bits of the same value should automatically insert a complementary bit. Likewise, a Receiver that receives five consecutive bits should treat the next bit as a stuff bit. Bit stuffing is applied to the following fields: SOF, Arbitration Field, Control Field, Data Field, and CRC Sequence (see Section 25.3.2 for more details).

- **Multi-cast:** All nodes receive the same bits as they are connected to the same bus. Data is consistent across all nodes unless there is a bus error (See Section 25.3.3).

- **Multi-master:** Any node can initiate a transmission. If a transmission is already ongoing, a node will wait until the current transmission is over before beginning its own transmission.

- **Message-Priorities and Arbitration:** If two or more nodes simultaneously initiate a transmission, the TWAI protocol ensures that one node will win arbitration of the bus. The Arbitration Field of the message transmitted by each node is used to determine which node will win arbitration.

- **Error Detection and Signaling:** Each node will actively monitor the bus for errors, and signal the detection errors by transmitting an Error Frame.

- **Fault Confinement:** Each node will maintain a set of error counts that are incremented/decremented according to a set of rules. When the error counts surpass a certain threshold, a node will automatically eliminate itself from the network by switching itself off.

- **Configurable Bit Rate:** The bit rate for a single TWAI bus is configurable. However, all nodes within the same bus must operate at the same bit rate.

**Transmitters and Receivers:**
At any point in time, a TWAI node can either be a Transmitter or a Receiver.
- A node originating a message is a Transmitter. The node remains a Transmitter until the bus is idle or until the node loses arbitration. Note that multiple nodes can be Transmitter if they have yet to lose arbitration.

**All nodes that are not Transmitters are Receivers.**

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version:** ESP32 TRM (Version 5.6)