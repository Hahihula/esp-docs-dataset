

```markdown
3. A dominant bit is detected at the eighth (last) bit of an Error Delimiter. Note that in this case, TEC and REC will not be incremented (see Section 34.2.3 for more details).

Transmitting an overload frame due to one of the above cases must also satisfy the following rules:

* The start of an overload frame due to case 1 is only allowed to be started at the first bit time of an expected intermission.
* The start of an overload frame due to case 2 and 3 is only allowed to be started one bit after detecting the dominant bit.
* For case 1, a maximum of two overload frames may be generated.

### 34.2.2.3 Interframe Space

The Interframe Space acts as a separator between frames. Data frames and remote frames must be separated from preceding frames by an Interframe Space, regardless of the preceding frame’s type (data frame, remote frame, error frame, or overload frame). However, error frames and overload frames do not need to be separated from preceding frames.

Figure 34.2-4 shows the fields within an Interframe Space:

![Interframe Space Diagram](#)

**Table 34.2-4. Interframe Space**

| Interframe Space | Description |
|------------------|-------------|
| Intermission     | The Intermission field consists of three recessive bits. |
| Suspend Transmission | An Error Passive node that has just transmitted a message must include a Suspend Transmission field. This field consists of eight recessive bits. Error Active nodes should not include this field. |
| Bus Idle         | The Bus Idle field is of arbitrary length. Bus Idle ends when an SOF is transmitted. If a node has a pending transmission, the SOF should be transmitted at the first bit following the Intermission. |

### 34.2.3 TWAI Errors

#### 34.2.3.1 Error Types

Bus Errors in TWAI are categorized into the following types:

**Bit Error**

A Bit Error occurs when a node transmits a bit value (i.e., dominant or recessive) but detects an opposite bit (e.g., a dominant bit is transmitted but a recessive is detected). However, if the transmitted bit is recessive and is located in the Arbitration Field, ACK Slot, or Passive Error Flag, then detecting a dominant bit will not be considered as a Bit Error.
```