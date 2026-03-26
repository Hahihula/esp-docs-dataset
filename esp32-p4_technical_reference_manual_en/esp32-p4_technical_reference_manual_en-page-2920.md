

```markdown
## 58.5.3 Master-Slave Mode

The TX and RX units can function as both master and slave.

When the TX unit serves as master, it is necessary to set the internal free-running clock as the clock source.
The TX unit drives TXD on the rising edge of the clock.

When the TX unit functions as a slave device, there are three scenarios, as shown in the table below.

Table 58.5-2. Requirements for TX Unit Operating as Slave with Clock Restrictions

| Clock Sent by Master | Clock Waveform                | Requirement                                                                 |
|----------------------|-------------------------------|-----------------------------------------------------------------------------|
| Free-running clock   | Any waveform                  | There is no requirement for the sampling edge of the master clock.          |
| Not free-running clock | Positive waveform (Figure 58.5-2) | The master clock should sample TXD at the falling edge.                     |
| Not free-running clock | Negative waveform (Figure 58.5-3) | The master device should invert the original clock and convert it to the waveform as Figure 58.5-2 shows before output.

Figure 58.5-2. Positive Waveform

Figure 58.5-3. Negative Waveform
```

When the RX unit serves as the master, it is required to set the clock source as the internal free-running clock.
The RX unit drives RXD on the rising edge of the clock.

When the RX unit functions as the slave, there are three scenarios, as shown in the table below.