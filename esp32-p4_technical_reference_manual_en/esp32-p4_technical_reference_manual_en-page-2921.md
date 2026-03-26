

```markdown
| Clock Sent by Master | Clock Restriction Clock Waveform | Requirement |
|---|---|---|
| Free-running clock | Any waveform | There is no requirement for the sampling edge of the master clock, and the valid data is subject to the external enable signal. |
| Not free-running clock | Positive waveform (Figure 58.5-2) | It is required for the master device to drive the data at the rising edge and the RX unit to sample the data at the falling edge (i.e., to inverse the master clock). |
| Not free-running clock | Negative waveform (Figure 58.5-3) | It is required for the master device to drive the data at the falling edge and the RX unit to sample the data at the rising edge (i.e., to use the original master clock). |

## 58.5.4 Receive Modes of the RX Unit

PARLIO supports eight receive modes, which can be divided into three major categories according to the enable signal:

*   Level Enable mode: data received is enabled by the external signal level;
*   Pulse Enable mode: data received is enabled by the external signal pulse;
*   Software Enable mode: the enable signal of data received can be configured by users directly.

The RX unit also supports inverse of the external enable signal. If the external enable signal is active-low, users can enable the function by setting `PARL_IO_RX_EXT_EN_INV` to switch to the corresponding receive mode introduced as follows.

### 58.5.4.1 Level Enable Mode

Figure 58.5-4 shows the Level Enable mode. In this mode, an active level on the external enable signal must be aligned with valid data. Since the external level enable signal occupies one IO pin, there are at most 15 IO pins left usable for RXD.

| Mode | Sub-mode | Description |
|---|---|---|
| LEVEL_ENABLE | \ | signal level high Valid data → |

Figure 58.5-4. Level Enable Mode for RX Unit

### 58.5.4.2 Pulse Enable Mode

Pulse Enable mode can be divided into six sub-modes depending on the pulse active level and its alignment with valid data. For detailed classification, see Figure 58.5-5.

Sub-modes 1 ~ 4 all contain start pulse and end pulse. The difference lies in whether start pulse and end pulse are aligned with valid data.
```