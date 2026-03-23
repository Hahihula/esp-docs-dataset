

```markdown
| Error Frame | Description |
|-------------|-------------|
| Error Flag | The Error Flag has two forms, the Active Error Flag consisting of 6 dominant bits and the Passive Error Flag consisting of 6 recessive bits (unless overridden by dominant bits of other nodes). Active Error Flags are sent by error active nodes, whilst Passive Error Flags are sent by error passive nodes. |
| Error Flag Superposition | The Error Flag Superposition field meant to allow for other nodes on the bus to transmit their respective Active Error Flags. The superposition field can range from 0 to 6 bits, and ends when the first recessive bit is detected (i.e., the first it of the Delimiter). |
| Error Delimiter | The Delimiter field marks the end of the error/overload frame, and consists of 8 recessive bits. |

## Overload Frames

An overload frame has the same bit fields as an error frame containing an Active Error Flag. The key difference is in the cases that can trigger the transmission of an overload frame. Figure 31.2-3 below shows the bit fields of an overload frame.

| Overload Frame | Description |
|----------------|-------------|
| Overload Flag (6 bits) | Consists of 6 dominant bits. Same as an Active Error Flag. |
| Overload Flag Superposition (0 to 6 bits) | Allows for the superposition of Overload Flags from other nodes, similar to an Error Flag Superposition. |
| Overload Delimiter (8 bits) | Consists of 8 recessive bits. Same as an Error Delimiter. |

Overload frames will be transmitted under the following cases:
1. A receiver requires a delay of the next data or remote frame.
2. A dominant bit is detected at the first and second bit of intermission.
```