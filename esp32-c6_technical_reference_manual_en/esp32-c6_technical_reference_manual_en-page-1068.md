

```markdown
| Data/Remote Frames | Description                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SOF                | The SOF (Start of Frame) is a single dominant bit used to synchronize nodes on the bus.                                                                                                                       |
| Base ID            | The Base ID (ID.28 to ID.18) is the 11-bit identifier for SFF, or the first 11 bits of the 29-bit identifier for EFF.                                                                                         |
| RTR                | The RTR (Remote Transmission Request) bit indicates whether the message is a data frame (dominant) or a remote frame (recessive). This means that a remote frame will always lose arbitration to a data frame if they have the same ID. |

Cont'd on next page
```