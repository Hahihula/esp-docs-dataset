

```markdown
| Clock Restriction | Clock Waveform | Requirement |
|:------------------------|:----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Clock Sent by Master | Clock Waveform | Requirement |
| Free-running clock | Any waveform | There is no requirement for the sampling edge of the master clock. |
| Not free-running clock | Positive waveform (Figure 43.5-2) | The master clock should sample TXD at the falling edge. |
| Not free-running clock | Negative waveform (Figure 43.5-3) | The master device should invert the original clock and convert it to the waveform as Figure 43.5-2 shows before output. |

**Figure 43.5-2. Positive Waveform**

**Figure 43.5-3. Negative Waveform**

When the RX unit serves as the master, it is required to set the clock source as the internal free-running clock. The RX unit drives RXD on the rising edge of the clock.

When the RX unit functions as the slave, there are three scenarios, as shown in the table below.

**Table 43.5-3. Requirements for RX Unit Operating as Slave with Clock Restrictions**

| Clock Restriction | Clock Waveform | Requirement |
|:------------------------|:----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Clock Sent by Master | Clock Waveform | Requirement |
| Free-running clock | Any waveform | There is no requirement for the sampling edge of the master clock, and the valid data is subject to the external enable signal. |
| Not free-running clock | Positive waveform (Figure 43.5-2) | It is required for the master device to drive the data at the rising edge and the RX unit to sample the data at the falling edge (i.e., to inverse the master clock). |
| Not free-running clock | Negative waveform (Figure 43.5-3) | It is required for the master device to drive the data at the falling edge and the RX unit to sample the data at the rising edge (i.e., to use the original master clock). |

## 43.5.4 Receive Modes of the RX Unit

PARLIO supports 8 receive modes, which can be divided into three major categories according to the enable signal:

*   Level Enable mode: data received is enabled by the external signal level;
```