

```markdown
## 31.2.2 TWAI Messages

TWAI nodes use messages to transmit data, and signal errors to other nodes when detecting errors on the bus.
Messages are split into various frame types, and some frame types will have different frame formats.

The TWAI protocol has of the following frame types:

* Data frame
* Remote frame
* Error frame
* Overload frame
* Interframe space

The TWAI protocol has the following frame formats:

* Standard Frame Format (SFF) that uses a 11-bit identifier
* Extended Frame Format (EFF) that uses a 29-bit identifier

### 31.2.2.1 Data Frames and Remote Frames

Data frames are used by nodes to send data to other nodes, and can have a payload of 0 to 8 data bytes.
Remote frames are used for nodes to request a data frame with the same identifier from other nodes, and thus
they do not contain any data bytes. However, data frames and remote frames share many fields. Figure 31.2-1
illustrates the fields and sub-fields of different frames and formats.

**Arbitration Field**

When two or more nodes transmits a data or remote frame simultaneously, the arbitration field is used to
determine which node will win arbitration of the bus. In the arbitration field, if a node transmits a recessive bit
while detects a dominant bit, this indicates that another node has overridden its recessive bit. Therefore, the
node transmitting the recessive bit has lost arbitration of the bus and should immediately switch to be a
receiver.

The arbitration field primarily consists of a frame identifier that is transmitted from the most significant bit first.
Given that a dominant bit represents a logical 0, and a recessive bit represents a logical 1:

* A frame with the smallest ID value always wins arbitration..
* Given the same ID and format, data frames always prevail over remote frames due to their RTR bits being
dominant.
* Given the same first 11 bits of ID, a Standard Format Data Frame always prevails over an Extended Format
Data Frame due to its SRR bits being recessive.

**Control Field**

The control field primarily consists of the DLC (Data Length Code) which indicates the number of payload data
bytes for a data frame, or the number of requested data bytes for a remote frame. The DLC is transmitted from
the most significant bit first.

**Data Field**

The data field contains the actual payload data bytes of a data frame. Remote frames do not contain any data
field.
```