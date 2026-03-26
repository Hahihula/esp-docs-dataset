

```markdown
| Mode       | Sub-mode                  | Description                                                                 |
|------------|----------------------------|-----------------------------------------------------------------------------|
|            | sub-mode1                 | pulse start(data bit include) && pulse end(data bit include)<br>Valid data → |
| PULSE_ENABLE| sub-mode2                 | pulse start(data bit include) && pulse end(data bit exclude)<br><← Valid data → |
|            | sub-mode3                 | pulse start(data bit exclude) && pulse end(data bit include)<br><← Valid data → |
|            | sub-mode4                 | pulse start(data bit exclude) && pulse end(data bit exclude)<br><← Valid data → |
|            | sub-mode5                 | pulse start(data bit include) && length end<br><← Valid data →               |
|            | sub-mode6                 | pulse start(data bit exclude) && length end<br><← Valid data →               |

Figure 58.5-5. Sub-Modes of Pulse Enable Mode for RX Unit

## 58.5.4.3 Software Enable Mode

The enable signal in Software Enable mode is determined by the internal configuration register. If users switch to this mode, the receive will only be activated when both `PARL_IO_RX_SW_EN` and `PARL_IO_RX_START` are set to 1.

Since the enable signal does not occupy IO pins on the interface, there are at most 16 IO pins usable by the RXD. Due to the differences of clock domains, the enable signal cannot be aligned with valid data. Thus, the validity of data needs to be identified by the valid clock edge. In this case, the RX Core clock needs to be aligned with valid data.

| Mode       | Sub-mode | Description |
|------------|----------|-------------|
| SW_ENABLE  | /        | Valid data → |

Figure 58.5-6. Software Enable Mode for RX Unit
```