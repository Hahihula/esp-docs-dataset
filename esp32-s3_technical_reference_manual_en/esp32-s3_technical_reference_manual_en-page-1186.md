**Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Title:**
31.3 Functional Protocol

**Subsection Title and Content:**
31.3.1 TWAI Properties

The TWAI protocol connects two or more nodes in a bus network, and allows nodes to exchange messages in a latency bounded manner. A TWAI bus has the following properties.

- **Single Channel and Non-Return-to-Zero:** The bus consists of a single channel to carry bits; thus communication is half-duplex. Synchronization is also implemented in this channel, so extra channels (e.g., clock or enable) are not required. The bit stream of a TWAI message is encoded using the Non-Return-to-Zero (NRZ) method.

- **Bit Values:** The single channel can either be in a dominant or recessive state; representing a logical 0 and a logical 1 respectively. A node transmitting data in a dominant state will always override another node transmitting data in a recessive state. The physical implementation on the bus is left to the application level to decide (e.g., differential pair of single wire).

- **Bit Stuffing:** Certain fields of TWAI messages are bit-stuffed. A transmitter that transmits five consecutive bits of the same value should automatically insert a complementary bit. Likewise, a receiver that receives five consecutive bits should treat the next bit as a stuffed bit. Bit stuffing is applied to the following fields: SOF (Start Of Frame), arbitration field, control field, data field, and CRC sequence.

- **Multi-cast:** All nodes receive the same bits; they are connected across all nodes unless there’s an error in bus communication or transmission errors occur as per Section 31.3.2 for more details).

- **Multi-master:** Any node can initiate a transmission if it is already ongoing, and will wait until current transmission completes before beginning its own.

**Additional Properties:**
- Message Priorities and Arbitration
- Error Detection and Signaling:
- Fault Confinement:

**Transmitters and Receivers:**

At any point in time; A TWAI node can either be a transmitter or receiver.
- **A note:** Originating message is transmits. The mode remains as long the bus idle until it loses arbitration.

All nodes that are not transmitters, receivers

**Footer Information:**
Espressif Systems
1186 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback