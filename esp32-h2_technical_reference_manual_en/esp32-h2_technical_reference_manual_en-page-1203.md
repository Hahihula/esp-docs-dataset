

```markdown
| Clock Sent by Master | Clock Waveform | Requirement |
|:----------------------|:----------------|:-----------------------------------------------------------------------------------------------------------------------------|
| Free-running clock    | Any waveform    | There is no requirement for the sampling edge of the master clock. |
| Not free-running clock| Positive waveform (Figure 38.5-2) | The master clock should sample TXD at the falling edge. |
| Not free-running clock| Negative waveform (Figure 38.5-3) | The master device should invert the original clock and convert it to the waveform as Figure 38.5-2 shows before output. |

**Figure 38.5-2. Positive Waveform**

**Figure 38.5-3. Negative Waveform**
```

```markdown
| Clock Sent by Master | Clock Waveform | Requirement |
|:----------------------|:----------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Free-running clock    | Any waveform    | There is no requirement for the sampling edge of the master clock, and the valid data is subject to the external enable signal. |
| Not free-running clock| Positive waveform (Figure 38.5-2) | It is required for the master device to drive the data at the rising edge and the RX unit to sample the data at the falling edge (i.e., to inverse the master clock). |
| Not free-running clock| Negative waveform (Figure 38.5-3) | It is required for the master device to drive the data at the falling edge and the RX unit to sample the data at the rising edge (i.e., to use the original master clock). |
```

## 38.5.4 Receive Modes of the RX Unit

PARLIO supports eight receive modes, which can be divided into three major categories according to the enable signal:

*   Level Enable mode: data received is enabled by the external signal level;
```