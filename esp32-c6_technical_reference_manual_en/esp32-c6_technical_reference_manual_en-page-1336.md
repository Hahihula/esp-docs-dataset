

```markdown
| Mode         | Sub-mode                                                                 Description                                                                                                                                 |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              | sub-mode 1                                                                   pulse start(data bit include) & pulse end(data bit include)<br><img>Valid data →<br><sub>←</sub>                                                                                   |
| PULSE_ENABLE | sub-mode 2                                                                   pulse start(data bit include) & pulse end(data bit exclude)<br><img>Valid data →<br><sub>←</sub>                                                                                   |
|              | sub-mode 3                                                                   pulse start(data bit exclude) & pulse end(data bit include)<br><img>Valid data →<br><sub>←</sub>                                                                                   |
|              | sub-mode 4                                                                   pulse start(data bit exclude) & pulse end(data bit exclude)<br><img>Valid data →<br><sub>←</sub>                                                                                   |
|              | sub-mode 5                                                                   pulse start(data bit include) & pulse end(data bit include)<br><img>Valid data →<br><sub>←</sub>                                                                                   |
|              | sub-mode 6                                                                   pulse start(data bit include) & pulse end(data bit exclude)<br><img>Valid data →<br><sub>←</sub>                                                                                   |
|              | sub-mode 7                                                                   pulse start(data bit exclude) & pulse end(data bit include)<br><img>Valid data →<br><sub>←</sub>                                                                                   |
|              | sub-mode 8                                                                   pulse start(data bit exclude) & pulse end(data bit exclude)<br><img>Valid data →<br><sub>←</sub>                                                                                   |
|              | sub-mode 9                                                                   pulse start(data bit include) & length end<br><img>Valid data →<br><sub>←</sub>                                                                                                           |
|              | sub-mode 10                                                                  pulse start(data bit exclude) & length end<br><img>Valid data →<br><sub>←</sub>                                                                                                          |
|              | sub-mode 11                                                                  pulse start(data bit include) & length end<br><img>Valid data →<br><sub>←</sub>                                                                                                          |
|              | sub-mode 12                                                                  pulse start(data bit exclude) & length end<br><img>Valid data →<br><sub>←</sub>                                                                                                          |

Figure 38.5-5. Sub-Modes of Pulse Enable Mode for RX Unit
```

### 38.5.4.3 Software Enable Mode

The enable signal in Software Enable mode is determined by the internal configuration register. If users switch to this mode, the receive will only be activated when both `PARL_IO_RX_SW_EN` and `PARL_IO_RX_START` are set to 1.

Since the enable signal does not occupy IO pins on the interface, there are at most 16 IO pins usable by the RXD. Due to the differences of clock domains, the enable signal cannot be aligned with valid data. Thus, the validity of data needs to be identified by the valid clock edge. In this case, the RX Core clock needs to be aligned with valid data.
```