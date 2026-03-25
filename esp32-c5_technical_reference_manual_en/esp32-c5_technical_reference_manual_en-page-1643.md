
```markdown
- Pulse Enable mode: data received is enabled by the external signal pulse;
- Software Enable mode: the enable signal of data received can be configured by users directly.

The RX unit also supports inverse of the external enable signal. If the external enable signal is active-low, users can enable the function by setting `PARL_IO_RX_EXT_EN_INV` to switch to the corresponding receive mode introduced as follows.

### 43.5.4.1 Level Enable Mode

Figure 43.5-4 shows the Level Enable mode. In this mode, an active level on the external enable signal must be aligned with valid data. Since the external level enable signal occupies one IO pin, there are at most 7 IO pins left usable for RXD.

| Mode          | Sub-mode             | Description                                                                 |
|---------------|----------------------|-----------------------------------------------------------------------------|
|               |                      | `signal level high`                                                        |
| LEVEL_ENABLE  | sub-mode 1           | Valid data →                                                               |
|               |                      |                                                                             |
|               | sub-mode 2           | `signal level low`                                                         |
|               |                      | Valid data →                                                               |

Figure 43.5-4. Sub-Modes of Level Enable Mode for RX Unit

### 43.5.4.2 Pulse Enable Mode

Pulse Enable mode can be divided into 6 sub-modes depending on the pulse active level and its alignment with valid data. For detailed classification, see Figure 43.5-5.

Sub-modes 1 ~ 4 all contain start pulse and end pulse. The difference lies in whether start pulse and end pulse are aligned with valid data.

Sub-modes 5 ~ 6 only contain start pulse and the end of valid data is signaled by configuring `PARL_IO_RX_BITLEN`.

Since the external pulse enable signal occupies one IO pin, there are at most 7 IO pins left usable for RXD. However, in sub-modes 4 and 6, as the data is considered valid before the pulse’s first edge and after the pulse’s last edge, the enable signal IO pin can serve as a data IO pin at the same time. Therefore, there are 8 IO pins usable for RXD in these two sub-modes.
```