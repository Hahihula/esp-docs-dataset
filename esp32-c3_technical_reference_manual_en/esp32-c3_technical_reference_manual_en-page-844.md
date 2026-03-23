

```markdown
## 33.3.1 RMT Architecture

Figure 33.3-1. RMT Architecture

The RMT module has four independent channels, two of which are TX channels and the other two are RX channels. Each TX channel has its own clock-divider counter, state machine, and transmitter. Each RX channel also has its own clock-divider counter, state machine, and receiver. The four channels share a 192 × 32-bit RAM.

## 33.3.2 RMT RAM

Figure 33.3-2. Format of Pulse Code in RAM

Figure 33.3-2 shows the format of pulse code in RAM. Each pulse code contains a 16-bit entry with two fields, level and period.
```